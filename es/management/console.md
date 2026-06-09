# Consola y controles de energía

La **Consola** es la interfaz principal para interactuar directamente con tu servidor de juegos. En esta guía, aprenderá cómo monitorear el uso del hardware, enviar comandos de juegos y administrar los estados de energía de su servidor.

---

## Controles de energía (botones de acción)

En la esquina superior derecha o barra lateral del tablero de la consola, encontrará cuatro botones principales de control de energía:

* **Inicio:** Enciende el contenedor del servidor e inicia el proceso del juego. Utilízalo si tu servidor está actualmente "fuera de línea".
* **Detener:** Envía una señal de apagado elegante al juego (por ejemplo, ejecutando `/stop` o `/save-all` en Minecraft). Esto guarda su progreso y apaga el servidor de forma segura.
* **Reiniciar:** Detiene elegantemente el juego y lo reinicia inmediatamente. Ideal para aplicar cambios de configuración o borrar caché de RAM.
* **Matar:** Finaliza instantáneamente el proceso del juego sin guardar.
  > [!CAUTION] 
  > **Utilice "Kill" únicamente si su servidor está completamente congelado o no responde al comando "Detener".** El uso de Kill con regularidad puede dañar archivos, revertir el progreso de su mundo o corromper entradas de bases de datos.

---

## Gráficos de monitoreo en tiempo real

El panel Reviactyl muestra gráficos continuos en tiempo real que representan la utilización de recursos de su servidor:

1. **Uso de CPU:** El porcentaje de potencia de procesamiento que se utiliza. Si permanece cerca del 100% durante períodos prolongados, los jugadores pueden experimentar un retraso (considere optimizar complementos, modificaciones o actualizar su plan).
2. **Uso de memoria (RAM):** Muestra la memoria actual asignada en comparación con el límite de su plan (por ejemplo, `4 GB / 8 GB`). 
   * *Si el servidor excede su límite de memoria, el asesino OOM (Memoria insuficiente) incorporado en el panel detendrá automáticamente el servidor para proteger la estabilidad del nodo. Optimice los archivos de su juego o actualice su plan si alcanza este límite con frecuencia.*
3. **Uso del disco:** Espacio de almacenamiento total consumido por los archivos de tu juego (mods, mundos, registros, copias de seguridad). Asegúrese de eliminar archivos de registro antiguos (`latest.log`, `debug.log`) o copias de seguridad antiguas para liberar espacio en el disco.

---

## Envío de comandos de consola

Debajo de la pantalla negra activa del terminal, hay una barra de comandos de texto etiquetada **"Escriba un comando..."**:

* Puedes escribir cualquier comando aquí para controlar el juego directamente desde la consola sin necesidad de privilegios de administrador en el juego.
* **No anteponga comandos con una barra diagonal (`/`)**. Por ejemplo, escriba `op PlayerName` o `say Hello World` y presione Entrar.
* Cualquier respuesta o error del servidor del juego se imprimirá en tiempo real en el registro de la consola anterior.