# Administrador de archivos web

El **Administrador de archivos** (que se encuentra en la pestaña **Archivos** en el menú de la barra lateral) le permite administrar todos los datos de su servidor directamente desde su navegador web sin necesidad de software externo.

---

## Operaciones básicas de archivos

Cuando abra el Administrador de archivos, verá el directorio raíz de su servidor. Desde aquí, puedes realizar varias acciones principales:

* **Crear archivos y carpetas:** Haga clic en los botones **"Crear archivo"** o **"Nueva carpeta"** en la esquina superior derecha.
* **Editar archivos:** Haga clic en cualquier archivo basado en texto (como `.yml`, `.json`, `.conf`, `.properties` o `.txt`). Esto abre un **editor de código integrado** con resaltado de sintaxis. Después de realizar los cambios, haga clic en **"Guardar contenido"** en la parte inferior.
* **Cargar archivos:** Arrastre y suelte archivos desde su computadora directamente a la ventana del navegador, o haga clic en el botón **"Cargar"** para buscar y seleccionar archivos.
  > [!TIP] 
  > El administrador de archivos web es perfecto para editar configuraciones individuales o cargar archivos más pequeños (menos de 100 MB). Para transferencias más grandes (como mapas completos, mundos o paquetes de mods grandes), recomendamos conectarse a través de **SFTP**.

---

## Menú de acción (Los tres puntos `...`)

A la derecha de cada archivo y carpeta, encontrará un botón de tres puntos `...` que abre el menú de acciones:

1. **Cambiar nombre:** Cambia el nombre de un archivo o directorio.
2. **Mover/Copiar:** Reubicar el archivo. Puede mover archivos proporcionando su ruta relativa (por ejemplo, mover `server.properties` a una carpeta ingresando `backup-configs/server.properties`).
3. **Descargar:** Guarde el archivo directamente en su computadora.
4. **Eliminar:** Elimina permanentemente el archivo o carpeta del almacenamiento del servidor.
   > [!WARNING] 
   > La eliminación de archivos es permanente y no se puede deshacer. Cree una copia de seguridad de su servidor antes de realizar eliminaciones masivas.

---

## Comprimir y extraer archivos (.zip)

Cargar carpetas que contienen cientos de archivos pequeños individuales (como paquetes de modificaciones o configuraciones de complementos) uno por uno es muy ineficiente. En lugar de eso:

1. Comprima la carpeta de su computadora en un archivo `.zip`.
2. Cargue el único archivo `.zip` al panel (a través del Administrador de archivos web o SFTP).
3. En el Administrador de archivos web, haga clic en los tres puntos `...` junto al archivo `.zip` cargado.
4. Seleccione **"Desarchivar"** o **"Descomprimir"**. El panel extraerá todos los archivos y subcarpetas al instante.
5. *(Opcional)* Elimine el archivo `.zip` cargado para ahorrar espacio en el disco.

También puede comprimir archivos en el panel seleccionándolos usando las casillas de verificación de la izquierda, haciendo clic en el botón **"Archivar"** en la parte superior y descargando el archivo `.zip` resultante.