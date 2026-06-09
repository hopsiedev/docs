# Subusuarios y permisos

Si está ejecutando un servidor con un equipo, es posible que desee brindarles a sus constructores, desarrolladores o copropietarios acceso al panel del servidor. La función **Subusuarios** te permite invitar a otros jugadores a tu panel con permisos específicos y granulares, lo que garantiza que solo accedan a lo que necesitan.

---

## 1. Invitar a un subusuario

Para agregar un nuevo subusuario:

1. Inicie sesión en el panel en [panel.vellix.host](https://panel.vellix.host) y seleccione su servidor.
2. Haga clic en la pestaña **"Usuarios"** en el menú de navegación de la barra lateral.
3. Haga clic en el botón **"Crear nuevo"** en la esquina superior derecha.
4. Complete el formulario de invitación:
   * **Correo electrónico del usuario:** Ingrese la dirección de correo electrónico exacta de la persona que desea invitar.
     * *Nota: Si aún no tienen una cuenta en el panel, recibirán una invitación por correo electrónico para configurar su contraseña y registrarse.*
   * **Permisos:** Seleccione las casillas correspondientes a los permisos que desea otorgarles.

---

## 2. Gestión de permisos granulares

Puede personalizar exactamente lo que cada subusuario puede hacer en su servidor. Los permisos se dividen en categorías lógicas:

### Consola de control
* **Controlar el estado de energía:** Permite iniciar, detener, reiniciar y cerrar el servidor.
* **Enviar comandos:** Permite escribir y enviar comandos en la barra de comandos de la consola en vivo.

### Gestión de archivos
* **Leer archivos:** Permite ver directorios y abrir archivos para leer contenidos.
* **Escribir archivos:** Permite editar archivos, crear nuevos y cargar carpetas.
* **Eliminar archivos:** Permite eliminar archivos y carpetas.
* **Detalles SFTP:** Permite ver los detalles de la conexión SFTP (se conectarán usando su propio nombre de usuario y contraseña del panel).

### Bases de datos y copias de seguridad
* **Crear Bases de Datos:** Permite crear y eliminar bases de datos MySQL.
* **Ver contraseña de la base de datos:** Permite revelar las credenciales de conexión de la base de datos.
* **Crear copias de seguridad:** Permite realizar copias de seguridad manuales del servidor.
* **Restaurar copias de seguridad:** Permite revertir archivos del servidor utilizando una copia de seguridad existente.

### Configuraciones y horarios
* **Crear Horarios:** Permite programar tareas (reinicios, copias de seguridad, envío de mensajes automáticos).
* **Editar configuración de inicio:** Permite modificar variables de entorno y opciones de comandos de inicio.

---

## 3. Revocar o editar el acceso

Puedes modificar los permisos de un subusuario o eliminar su acceso por completo en cualquier momento:

* **Para editar permisos:** Vaya a la pestaña **"Usuarios"**, haga clic en el ícono de edición (lápiz) al lado del correo electrónico del subusuario, marque/desmarque los permisos y haga clic en **"Guardar"**.
* **Para revocar el acceso:** Haga clic en el ícono de eliminar (papelera) al lado del correo electrónico del subusuario. Su acceso al panel de su servidor finalizará inmediatamente.