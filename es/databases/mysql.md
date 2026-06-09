# Bases de datos MySQL

Muchos complementos y modificaciones de juegos (como *LuckPerms*, *CoreProtect*, *Dynmap* o sistemas de registro personalizados) requieren una base de datos **MySQL/MariaDB** para almacenar datos del jugador, permisos o bloquear ediciones de forma rápida y confiable, en lugar de almacenarlos en archivos planos locales `.json` o `.db` que pueden ralentizar el rendimiento de su servidor.

Con Vellix Hosting, puede aprovisionar y administrar bases de datos MySQL con un solo clic directamente desde su panel Reviactyl.

---

## 1. Creando una Base de Datos en el Panel

Para crear una nueva base de datos:

1. Acceda al panel de su servidor en el panel en [panel.vellix.host](https://panel.vellix.host).
2. Haga clic en la pestaña **"Bases de datos"** en el menú de navegación de la barra lateral.
3. Haga clic en el botón **"Crear base de datos"** en la esquina superior derecha.
4. Complete los campos:
   * **Nombre de la base de datos:** Proporcione un nombre descriptivo breve para la base de datos (por ejemplo, `luckperms` o `playerdata`).
   * **Conexiones desde:** Establezca esto en `%` (signo de porcentaje) para permitir conexiones desde cualquier host (esta es la configuración más flexible y evita problemas de firewall si se conecta desde fuera del nodo, por ejemplo, servidores web o proxies BungeeCord).
5. Haga clic en el botón **"Crear base de datos"**.

La base de datos se creará instantáneamente y se agregará a la lista.

---

## 2. Recuperación de credenciales de base de datos

Una vez creada tu base de datos, verás una tarjeta con los parámetros de conexión. Haga clic en el icono de candado para revelar la contraseña:

* **Host/Punto final:** La dirección IP o dominio del servidor de base de datos (por ejemplo, `mysql.vellix.host` o una IP de nodo).
* **Nombre de la base de datos:** El nombre final generado por el panel, generalmente precedido por el ID de su servidor (por ejemplo, `s1_luckperms`).
* **Nombre de usuario:** El nombre de usuario de la base de datos generada automáticamente (por ejemplo, `u1_xYzA`).
* **Contraseña:** La contraseña única y segura generada para este usuario de la base de datos.
* **Puerto:** El puerto estándar de MySQL, que es `3306`.

---

## 3. Configurando su complemento (Ejemplo: LuckPerms)

Para conectar un complemento a su nueva base de datos, abra el archivo de configuración del complemento (generalmente `config.yml` o `config.conf`) en el **Administrador de archivos web**:

1. Busque `storage-method` o la configuración del tipo de almacenamiento y cámbielo de `h2` o `sqlite` a **`mysql`**.
2. Reemplace los marcadores de conexión con sus credenciales:

```yaml
# Typical MySQL database connection setup in Minecraft plugins
storage-method: mysql

address: "mysql.vellix.host:3306" # Enter the database Host and Port here
database: "s1_luckperms"          # Enter the generated Database Name
username: "u1_xYzA"               # Enter the Database Username
password: "your_secure_password"  # Enter the revealed Password
```

3. Guarde el archivo.
4. Reinicie su servidor de juegos desde la consola para establecer la conexión de la base de datos.

> [!NOTE] 
> El aprovisionamiento de la base de datos es completamente gratuito y el almacenamiento de la base de datos no cuenta para la asignación de disco de su servidor principal. Sin embargo, recomendamos mantener la higiene de la base de datos eliminando los registros antiguos periódicamente para garantizar un rendimiento óptimo de las consultas.