# Seguridad de la cuenta

Mantener su cuenta segura es esencial para proteger los archivos, las configuraciones y los reproductores de su servidor. En esta guía, aprenderá cómo **cambiar su contraseña** y habilitar la **Autenticación de dos factores (2FA)**.

---

## Changing Your Password

For safety, we strongly recommend changing the auto-generated temporary password you received in your welcome email as soon as possible.

### Steps to update your password:
1. Log in to the panel at [panel.vellix.host](https://panel.vellix.host).
2. Click on your profile avatar in the upper right-hand corner (or the account settings icon in the sidebar).
3. Select **"Account Settings"**.
4. Scroll to the **"Change Password"** section.
5. Enter your current password (the temporary one from your email).
6. Enter your new password and confirm it in the field below.
   * *Tip: Use a mix of uppercase, lowercase, numbers, and special symbols.*
7. Click the **"Update Password"** button.

> [!NOTE]
> Changing your password will log out all other active sessions for safety. You will need to use your new password for any future logins, as well as for your SFTP connection.

---

## Autenticación de dos factores (2FA)

La autenticación de dos factores agrega una capa adicional de seguridad. Cada vez que inicie sesión, se le solicitará su nombre de usuario, contraseña y un código de verificación dinámico de 6 dígitos generado por una aplicación en su teléfono.

### Pasos para habilitar 2FA:
1. Vaya a **"Configuración de la cuenta"**.
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
1. Visita [panel.vellix.host](https://panel.vellix.host).
2. Haga clic en **"¿Olvidó su contraseña?"** en la tarjeta de inicio de sesión.
3. Ingrese la dirección de correo electrónico de su cuenta y haga clic en **"Enviar enlace para restablecer contraseña"**.
4. Siga el enlace enviado a su correo electrónico para configurar una nueva contraseña.
