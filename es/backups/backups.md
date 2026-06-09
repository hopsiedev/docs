# Copias de seguridad y restauración

Proteger el progreso de su servidor es crucial. La pérdida de datos puede ocurrir debido a mods que no funcionan correctamente, archivos guardados dañados o errores de configuración. En esta guía, aprenderá cómo crear copias de seguridad manuales, restaurarlas y programar copias de seguridad automáticas.

---

## 1. Creación de una copia de seguridad manual

Siempre debes crear una copia de seguridad antes de realizar cambios importantes, actualizar versiones del juego o agregar nuevas modificaciones.

1. Vaya a su servidor en el panel en [panel.vellix.host](https://panel.vellix.host).
2. Haga clic en la pestaña **"Copias de seguridad"** en el menú de la barra lateral.
3. Haga clic en el botón **"Crear copia de seguridad"** en la esquina superior derecha.
4. Complete los campos:
   * **Nombre de la copia de seguridad:** Asigne a su copia de seguridad un nombre descriptivo (por ejemplo, *Antes de la actualización de Forge* o *Salvado mundial 2026*).
   * **Archivos y carpetas ignorados:** *(Opcional)* Ingrese rutas relativas a los archivos o carpetas que desea excluir de la copia de seguridad (por ejemplo, excluyendo la carpeta `backups/` o registros grandes como `logs/` para ahorrar espacio). Cada regla debe ir en una nueva línea.
5. Haga clic en **"Iniciar copia de seguridad"**.

El panel empaquetará sus archivos en un archivo seguro en segundo plano. La tarjeta de respaldo mostrará una ruleta hasta que se complete por completo.

---

## 2. Restaurar o descargar una copia de seguridad

Una vez creada una copia de seguridad, haga clic en los tres puntos `...` en la tarjeta de respaldo para abrir el menú de acciones:

* **Restaurar:** Devuelve todos los archivos del servidor al estado en el que se encontraban cuando se realizó la copia de seguridad.
  > [!WARNING] 
  > **La restauración de una copia de seguridad sobrescribirá los archivos existentes.** Puede marcar la casilla *"Eliminar archivos antes de restaurar"* para limpiar el directorio del servidor y asegurarse de que no queden archivos antiguos y conflictivos antes de colocar los archivos de copia de seguridad.
* **Descargar:** Descarga el archivo de respaldo (`.tar.gz`) directamente a su computadora.
* **Bloquear/Desbloquear:** Bloquear una copia de seguridad evita que se elimine automática o manualmente por error cuando alcanzas el límite de copias de seguridad.
* **Eliminar:** Elimina permanentemente el archivo de respaldo para liberar espacio.

---

## 3. Programación de copias de seguridad automáticas

Crear copias de seguridad manualmente es útil, pero automatizar el proceso garantiza que nunca perderá el progreso, incluso si olvida ejecutarlas. Puede configurar una programación de respaldo en la pestaña **"Programaciones"**:

1. Haga clic en la pestaña **"Horarios"** en la barra lateral.
2. Haga clic en **"Crear programa"** en la esquina superior derecha.
3. Asigne un nombre a su programación (por ejemplo, *Copia de seguridad diaria*).
4. Establezca la frecuencia usando la notación Cron. Aquí hay ajustes preestablecidos comunes:
   * **Todos los días a medianoche:** Minutos: `0`, Horas: `0`, Día del mes: `*`, Mes: `*`, Día de la semana: `*`
   * **Cada 12 horas:** Minutos: `0`, Horas: `*/12`, Día del mes: `*`, Mes: `*`, Día de la semana: `*`
5. Haga clic en **"Crear programación"**.
6. Haga clic en el programa recién creado en la lista, luego haga clic en **"Nueva tarea"** en la parte superior derecha.
7. Cambie la **Acción** a **"Crear copia de seguridad"**.
8. Complete los archivos ignorados (si los hay) y haga clic en **"Crear tarea"**.

Su servidor ahora ejecutará copias de seguridad automáticas en el intervalo configurado.