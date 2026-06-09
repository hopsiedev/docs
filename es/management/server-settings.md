# Opciones de inicio y asignaciones de puertos

Para ejecutar modificaciones personalizadas, configurar sistemas de votación, configurar chats de voz o modificar la versión de Java que ejecuta su servidor, deberá administrar sus asignaciones de puertos y variables de inicio.

---

## 1. Asignaciones de puertos (configuraciones de red)

A su servidor se le asigna una IP y un puerto principales (por ejemplo, `190.22.44.112:25565`). Algunos complementos (como *Dynmap*, *Votifier* o *Simple Voice Chat*) requieren sus propios puertos adicionales para comunicarse.

### Cómo solicitar y asignar puertos adicionales:
1. Inicie sesión en [panel.vellix.host](https://panel.vellix.host) y seleccione su servidor.
2. Haga clic en la pestaña **"Red"** en el menú de la barra lateral.
3. Si tiene asignaciones disponibles, haga clic en **"Crear asignación"** (o abra un ticket de soporte en Discord si necesita puertos adicionales asignados a su nodo).
4. El nuevo puerto aparecerá en la lista.
5. En el archivo de configuración de su complemento, reemplace el puerto predeterminado con su nuevo puerto asignado (nunca use puertos aleatorios; solo use puertos específicamente asignados a su servidor en la pestaña Red).

---

## 2. Modificación de las opciones de inicio

La pestaña **"Inicio"** contiene variables de entorno clave que determinan cómo se inicia el ejecutable del servidor del juego:

* **Versión de Java:** Seleccione la versión del kit de desarrollo de Java (JDK).
  * **Java 8/11:** Para versiones anteriores de Minecraft (1.12.2 y anteriores).
  * **Java 17:** Estándar para Minecraft 1.18 a 1.20.4.
  * **Java 21:** Estándar para Minecraft 1.20.5 y superiores.
* **Archivo Jar del servidor:** El nombre del archivo que ejecutará el servidor (por ejemplo, `server.jar` o `vanilla.jar`). Asegúrese de que el archivo cargado en su Administrador de archivos tenga exactamente el mismo nombre que el ingresado aquí.
* **Variables de comando de inicio:** Indicadores personalizados, como jugadores máximos, puertos de consulta o versiones de servidor, según el juego.

> [!IMPORTANT] 
> Algunas variables de inicio están bloqueadas por el sistema para mantener la estabilidad. Si necesita realizar modificaciones en campos bloqueados o necesita indicadores de inicio personalizados (como los indicadores de rendimiento de Aikar), comuníquese con nuestro equipo de soporte en Discord.