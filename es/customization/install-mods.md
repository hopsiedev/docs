# Carga e instalación de mods/complementos

Personalizar su servidor con modificaciones, complementos o modos de juego personalizados es una de las mejores formas de mejorar la experiencia de juego. Esta guía lo guiará a través de la instalación de complementos individuales, modificaciones y paquetes de modificaciones de servidor completos en su servidor Vellix Hosting.

---

## 1. Complementos versus Mods: ¿Cuál usa mi servidor?

Antes de cargar archivos, debe saber qué admite el software de su servidor:
* **Complementos (Spigot, Paper, Purpur):** Amplíe la funcionalidad del servidor (como agregar prefijos de reclamos, economía o chat) sin requerir que los jugadores instalen nada en sus computadoras.
* **Modificaciones (Forge, Fabric, NeoForge):** Agregue bloques, elementos, criaturas y dimensiones personalizados. **Tanto el servidor como los jugadores deben tener exactamente los mismos mods instalados.**

---

## 2. Instalación de complementos o modificaciones individuales

1. Descargue los archivos `.jar` para los complementos/mods que desee utilizar de fuentes confiables (por ejemplo, CurseForge, Modrinth o SpigotMC).
   * *Asegúrate de que sean compatibles con la versión del juego que ejecuta tu servidor.*
2. Detenga su servidor desde la **Consola**.
3. Abra el **Administrador de archivos web** o conéctese a través de **SFTP**.
4. Navegue a la carpeta apropiada:
   * Para complementos Spigot/Paper/Purpur: cargue los archivos `.jar` en el directorio **`plugins/`**.
   * Para mods Forge/Fabric: sube los archivos `.jar` al directorio **`mods/`**.
5. Vuelva a la **Consola** y haga clic en **Iniciar** o **Reiniciar**.
6. Verifique que se cargaron correctamente:
   * En Minecraft, ejecuta el comando `plugins` en la consola (o `/plugins` en el juego) para ver tus complementos activos.

---

## 3. Instalación de un Modpack completo (por ejemplo, paquete de servidor CurseForge)

Para ejecutar un modpack preempaquetado (como RLCraft, Pixelmon o Better MC):

1. Descargue los archivos **Server Pack** para el modpack (normalmente un archivo `.zip` que contiene las carpetas `mods`, `config` y bibliotecas).
2. Detenga su servidor.
3. Abra su cliente **SFTP** y conéctese al servidor.
4. Si tiene archivos existentes, primero debe hacer una copia de seguridad y luego eliminarlos del directorio del servidor para evitar conflictos.
5. Cargue el archivo modpack `.zip` en el directorio raíz de su servidor.
6. Abra el **Administrador de archivos web** en su navegador, ubique el archivo `.zip` cargado, haga clic en los tres puntos `...` y elija **"Desarchivar"** para extraer todos los archivos.
7. Verifique la configuración de inicio:
   * En la pestaña **"Inicio"** en la barra lateral, asegúrese de haber seleccionado la **Versión de Java** correcta requerida por el modpack (por ejemplo, Java 17 para Minecraft 1.18+, Java 21 para Minecraft 1.20.5+).
   * Asegúrese de que el **Archivo Jar del servidor** o los parámetros de inicio coincidan con los requisitos del script de inicio del modpack.
8. Vuelva a la **Consola** y haga clic en **Iniciar**.

---

## Solución de problemas comunes

* **El servidor está atascado en un bucle de inicio:** Verifique el registro de la consola. Si ves `java.lang.UnsupportedClassVersionError`, significa que tu versión de Java está desactualizada o es demasiado nueva para la versión de tu juego. Cambie la versión de Java en la pestaña **Inicio**.
* **Error de dependencia faltante:** Algunas modificaciones o complementos requieren otras modificaciones de la biblioteca principal para funcionar. Lea la página de descripción del mod/complemento y cargue las dependencias que faltan en la carpeta de su servidor.
* **Modpack no carga bloques personalizados:** Verifique que haya cargado los archivos mod en el directorio `mods/` del servidor y que haya instalado exactamente la misma versión del modpack en su iniciador local (aplicación CurseForge, aplicación Modrinth, Prism Launcher).