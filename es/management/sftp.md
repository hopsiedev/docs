# Conexión SFTP (FileZilla / WinSCP)

Para transferir carpetas enteras, mapas pesados, paquetes de mods grandes o realizar modificaciones masivas en su servidor, el administrador de archivos web puede ser lento. Para estas tareas, utilizar un cliente **SFTP (Protocolo seguro de transferencia de archivos)** es la mejor opción.

---

## 1. Recupere sus credenciales SFTP

Cada servidor de juegos en Vellix Hosting tiene sus propios detalles de conexión SFTP únicos:

1. Inicie sesión en su servidor en el panel en [panel.vellix.host](https://panel.vellix.host).
2. Haga clic en la pestaña **"Configuración"** o **"SFTP"** en el menú de navegación de la barra lateral.
3. Ubique la sección **Detalles de SFTP** para encontrar:
   * **Dirección del servidor/Host:** La dirección del nodo que aloja su servidor (por ejemplo, `sftp.vellix.host` o una dirección IP).
   * **Puerto:** Generalmente `2022` (el puerto SFTP estándar para nuestro demonio de panel).
   * **Nombre de usuario:** Un identificador de usuario único con el formato `yourusername.serverid` (por ejemplo, `admin.a1b2c3d4`).
   * **Contraseña:** **Esta es exactamente la misma contraseña** que utiliza para iniciar sesión en el panel web.

---

## 2. Conexión con FileZilla (recomendado)

[FileZilla](https://filezilla-project.org/) es un cliente SFTP multiplataforma gratuito disponible para Windows, macOS y Linux.

### Pasos para conectarse:
1. Inicie FileZilla.
2. En la barra **Quickconnect** en la parte superior, complete los siguientes campos:
   * **Host:** Copie y pegue la *Dirección del servidor* del panel.
   * **Nombre de usuario:** Copie y pegue el *Nombre de usuario* del panel.
   * **Contraseña:** Ingrese la contraseña de su cuenta.
   * **Puerto:** Introduzca `2022`.
3. Haga clic en el botón **"Conexión rápida"**.
4. Si aparece un mensaje de advertencia sobre una *"Clave de host desconocida"*, marque la casilla *"Confiar siempre en este host"* y haga clic en **Aceptar**.
5. Una vez conectado, los archivos locales de su computadora se mostrarán a la izquierda y el directorio de su servidor remoto aparecerá a la derecha. Ahora puedes arrastrar y soltar archivos para transferirlos.

---

## 3. Conexión con WinSCP (solo Windows)

[WinSCP](https://winscp.net/) es una popular utilidad gratuita exclusiva de Windows para transferencias seguras.

### Pasos para conectarse:
1. Abra WinSCP.
2. En la ventana **Iniciar sesión**, configure lo siguiente:
   * **Protocolo de archivo:** Seleccione **SFTP**.
   * **Nombre de host:** Ingrese la *Dirección del servidor* desde el panel.
   * **Número de puerto:** Introduzca `2022`.
   * **Nombre de usuario:** Ingresa tu *Nombre de usuario* desde el panel.
   * **Contraseña:** Ingrese la contraseña de su cuenta.
3. Haga clic en **"Iniciar sesión"** (o haga clic en **"Guardar"** para almacenar esta sesión y facilitar el acceso en el futuro).
4. Acepte la advertencia de la clave del host del servidor en su primera conexión.

---

## Consejos esenciales para la transferencia

> [!TIP] 
> **Evite transferir carpetas sin formato con miles de archivos pequeños:** Los protocolos como SFTP requieren un protocolo de enlace para cada archivo. Transferir una carpeta con 2000 archivos mod directamente puede llevar horas. En su lugar, comprima la carpeta en su computadora, cargue el único archivo `.zip` a través de SFTP y luego use la opción **"Desarchivar"** del administrador de archivos web para extraerlo en segundos.

> [!WARNING] 
> Si actualiza la contraseña de su cuenta en el panel web (como se describe en la guía de seguridad), su contraseña SFTP se actualiza instantáneamente para coincidir con ella. ¡No olvide actualizar sus contraseñas de conexión guardadas en FileZilla o WinSCP!