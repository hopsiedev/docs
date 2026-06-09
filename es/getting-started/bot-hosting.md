---
title: "Hospedar Bots de Discord"
sidebarTitle: "Hospedar Bots"
description: "Aprende cómo hospedar y crear servidores gratuitos de bots de Discord en Vellix Hosting"
---

Vellix Hosting ofrece hospedaje gratuito de bots de Discord a través de la integración con nuestra comunidad de Discord. Sigue esta guía para configurar, implementar y configurar tu aplicación Node.js.

---

## Especificaciones del Servicio

Cuando creas un servidor gratuito de bots de Discord, obtienes:

* **Entorno de Ejecución Dedicado**: Entorno aislado de Node.js en un contenedor Docker.
* **Memoria (RAM)**: 250 MB de memoria RAM.
* **Almacenamiento**: 1 GB de almacenamiento SSD de alta velocidad.
* **Gestión**: Acceso completo a la consola y gestión de archivos FTP/SFTP.

---

## Guía de Inicio Rápido Paso a Paso

Sigue estos pasos para implementar tu bot:

### 1. Crea tu Servidor
Únete a nuestro servidor de Discord y ve al canal dedicado para tickets o creación de bots:
* **Canal de Discord**: [Soporte de Discord](https://discord.com/channels/1504707289385533461/1512867928717000876)
* Haz clic en el botón de creación de servidor.
* ⚠️ **Importante**: ¡Asegúrate de tener abiertos los mensajes directos (DMs) de Discord para que nuestro bot pueda enviarte tu contraseña temporal del panel!

### 2. Inicia Sesión en el Panel
* Accede al panel de control: [panel.vellix.host](https://panel.vellix.host)
* Inicia sesión con tu correo electrónico y la contraseña temporal enviada a tus DMs de Discord.
* (Opcional) Te recomendamos cambiar tu contraseña en la configuración de la cuenta de inmediato.

### 3. Sube los Archivos de tu Bot
* Selecciona tu servidor recién creado desde el panel principal.
* Ve a la pestaña **Administrador de Archivos** en la barra lateral.
* Sube los archivos de tu bot (por ejemplo, `index.js`, `package.json`, archivos `.env`).
* > [!CAUTION]
  > **NO subas la carpeta `node_modules`.** El panel instalará las dependencias automáticamente para ahorrar ancho de banda y almacenamiento.

### 4. Instala los Paquetes
* Ve a la pestaña **Consola**.
* Los paquetes se instalarán automáticamente desde tu `package.json` cuando inicies el servidor por primera vez, o puedes especificar opciones de inicio personalizadas.

### 5. Inicia tu Bot
* Configura tus variables de entorno, token y secretos en el panel de control.
* ¡Haz clic en el botón verde **Iniciar** en la Consola para arrancar tu bot!
