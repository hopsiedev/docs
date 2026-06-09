# Subusers & Permissions

If you are running a server with a team, you might want to give your builders, developers, or co-owners access to the server dashboard. The **Subusers** feature allows you to invite other players to your panel with specific, granular permissions, ensuring they only access what they need.

---

## 1. Inviting a Subuser

To add a new subuser:

1. Log in to the panel at [panel.vellix.host](https://panel.vellix.host) and select your server.
2. Click on the **"Users"** tab in the sidebar navigation menu.
3. Click the **"Create New"** button in the upper-right corner.
4. Fill out the invite form:
   * **User Email:** Enter the exact email address of the person you want to invite.
     * *Note: If they do not have an account on the panel yet, they will receive an email invitation to set up their password and register.*
   * **Permissions:** Select the checkboxes corresponding to the permissions you wish to grant them.

---

2. ## Managing Granular Permissions

You can customize exactly what each subuser can do on your server. Permissions are divided into logical categories:

### Control Console
* **Control Power State:** Allows starting, stopping, restarting, and killing the server.
* **Send Commands:** Allows typing and sending commands in the live console command bar.

### File Management
* **Read Files:** Allows viewing directories and opening files to read contents.
* **Write Files:** Allows editing files, creating new ones, and uploading folders.
* **Delete Files:** Allows deleting files and folders.
* **SFTP Details:** Allows viewing the SFTP connection details (they will connect using their own panel username and password).

### Databases & Backups
* **Create Databases:** Allows creating and deleting MySQL databases.
* **View Database Password:** Allows revealing database connection credentials.
* **Create Backups:** Allows taking manual server backups.
* **Restore Backups:** Allows reverting server files using an existing backup.

### Settings & Schedules
* **Create Schedules:** Allows scheduling tasks (restarts, backups, sending automatic messages).
* **Edit Startup Settings:** Allows modifying environment variables and startup command options.

---

3. ## Revoking or Editing Access

You can modify a subuser's permissions or remove their access entirely at any time:

* **To Edit Permissions:** Go to the **"Users"** tab, click the edit icon (pencil) next to the subuser's email, check/uncheck the permissions, and click **"Save"**.
* **To Revoke Access:** Click the delete icon (trash can) next to the subuser's email. Their access to your server dashboard will be terminated immediately.
