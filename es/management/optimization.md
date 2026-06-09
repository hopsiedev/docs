# Consejos de rendimiento y optimización del servidor

El retraso y las bandas elásticas pueden arruinar la experiencia del jugador. Si bien Vellix Hosting proporciona procesadores Ryzen 9 de alta frecuencia y SSD NVMe rápidos, el software de servidor no optimizado, las configuraciones de modificaciones pesadas o el recuento excesivo de entidades aún pueden degradar el rendimiento. 

Siga estos consejos de optimización profesional para mantener su servidor funcionando a una velocidad sólida de 20 TPS (Ticks por segundo).

---

## 1. Pregenera tu mundo (crítico para Minecraft)

Generar nuevos fragmentos sobre la marcha cuando los jugadores vuelan con Elytras o corren rápido es la causa número uno del retraso del servidor. Enfatiza los ciclos de lectura/escritura tanto de la CPU como del disco.

### Cómo pregenerar fragmentos:
1. Instale el complemento **Chunky** (compatible con Spigot, Paper, Fabric, Forge).
2. Detenga su servidor.
3. En `server.properties`, establezca el tamaño del borde mundial (por ejemplo, un radio de 5000 bloques).
4. Inicie el servidor y ejecute estos comandos en la **Consola**:
   * `chunky center 0 0` (establece el centro de generación).
   * `chunky radius 5000` (establece el radio de generación).
   * `chunky start` (inicia el proceso de generación).
5. Deje que Chunky complete la tarea antes de permitir que los jugadores se unan. Puede tardar varias horas dependiendo del radio. Una vez terminado, el retraso en la carga de fragmentos prácticamente se eliminará.

---

## 2. Optimizar los archivos de configuración del servidor

Si está ejecutando un servidor de Minecraft, use **Paper** o **Purpur** en lugar de Vanilla o Spigot. Contienen parches de rendimiento avanzados.

Abra los siguientes archivos en el **Administrador de archivos web** y ajuste estos valores:

### `server.properties`
* `view-distance=6` (Controla cuántos fragmentos se envían al cliente. Se recomiendan valores entre 6 y 8).
* `simulation-distance=4` (Controla qué fragmentos de entidades activas y ticks se ejecutan. Reducir esto a 4 o 5 reduce drásticamente la carga de la CPU).

### `paper-world-defaults.yml` (o `spigot.yml`)
* **Rangos de activación de entidades:** Reduce la distancia a la que actúan los animales, monstruos y elementos diversos.
* **Colisiones máximas de entidades:** Limite la cantidad de veces que las entidades verifican las colisiones por tick (por ejemplo, establezca `max-entity-collisions=2`).

---

## 3. Recolección de basura y consejos para la memoria

* **Utilice versiones modernas de Java:** Las versiones más nuevas de Java (como Java 21) tienen una recolección de basura superior (ZGC/G1GC) que reduce los picos de retraso durante la limpieza de la memoria.
* **Evita los paquetes de modificaciones inflados:** Cada modificación activa aumenta el uso de memoria. Elimine modificaciones solo estéticas que no sean críticas para el juego o modificaciones que realicen cálculos excesivos.
* **Monitorear registros de spam:** Si un complemento genera errores en su consola constantemente, escribirá miles de líneas en su disco, lo que generará un retraso en el disco. Repare la configuración o elimine el complemento defectuoso.