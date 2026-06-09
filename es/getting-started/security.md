# Seguridad de la cuenta

Mantener su cuenta segura es esencial para proteger los archivos, las configuraciones y los reproductores de su servidor. En esta guía, aprenderá cómo **cambiar su contraseña** y habilitar la **Autenticación de dos factores (2FA)**.

---

## Cambiando tu contraseña

Por seguridad, recomendamos encarecidamente cambiar la contraseña temporal generada automáticamente que recibió en su correo electrónico de bienvenida lo antes posible.

### Pasos para actualizar tu contraseña:
1. Inicie sesión en el panel en [panel.vellix.host](https://panel.vellix.host).
2. Haga clic en el avatar de su perfil en la esquina superior derecha (o en el ícono de configuración de la cuenta en la barra lateral).
3. Seleccione **"Configuración de cuenta"**.
4. Desplácese hasta la sección **"Cambiar contraseña"**.
5. Ingrese su contraseña actual (la temporal de su correo electrónico).
6. Ingrese su nueva contraseña y confírmela en el campo a continuación.
   * *Consejo: utilice una combinación de mayúsculas, minúsculas, números y símbolos especiales.*
7. Haga clic en el botón **"Actualizar contraseña"**.

> [!NOTE] 
> Al cambiar su contraseña, se cerrarán todas las demás sesiones activas por seguridad. Necesitará utilizar su nueva contraseña para futuros inicios de sesión, así como para su conexión SFTP.

---

## Autenticación de dos factores (2FA)

La autenticación de dos factores agrega una capa adicional de seguridad. Cada vez que inicie sesión, se le solicitará su nombre de usuario, contraseña y un código de verificación dinámico de 6 dígitos generado por una aplicación en su teléfono.

### Pasos para habilitar 2FA:
1. Navegue hasta **"Configuración de la cuenta"**.
2. Localice la sección **"Autenticación de dos factores"**.
3. Haga clic en el botón **"Habilitar"**.
4. Verá un **Código QR** y una clave de recuperación de respaldo.
5. Abra una aplicación de autenticación en su teléfono (como **Google Authenticator**, **Authy** o **Microsoft Authenticator**).
6. Escanea el código QR usando tu aplicación.
7. La aplicación generará un código de 6 dígitos que cambia cada 30 segundos.
8. Ingrese el código actual de 6 dígitos en el panel para confirmar.
9. Haga clic en **"Enviar"** o **"Activar"**.

> [!IMPORTANT] 
> **Guarde sus claves de recuperación en un lugar seguro y sin conexión.** Si pierde su teléfono o elimina la aplicación, necesitará las claves de recuperación para iniciar sesión. Sin ellas, tendrá que abrir un ticket de soporte en nuestro servidor de Discord y nuestro equipo deberá verificar manualmente su identidad antes de desactivar 2FA.

---

## Restablecer una contraseña olvidada

Si alguna vez olvidas tu contraseña:
1. Visite [panel.vellix.host](https://panel.vellix.host).
2. Haga clic en **"¿Olvidó su contraseña?"** en la tarjeta de inicio de sesión.
3. Ingrese la dirección de correo electrónico de su cuenta y haga clic en **"Enviar enlace para restablecer contraseña"**.
4. Siga el enlace enviado a su correo electrónico para configurar una nueva contraseña.