# SFTP Connection (FileZilla / WinSCP)

For transferring entire folders, heavy maps, large modpacks, or doing bulk modifications on your server, the web file manager can be slow. For these tasks, using a **SFTP (Secure File Transfer Protocol)** client is the best option.

---

## 1. Retrieve Your SFTP Credentials

Every game server on Vellix Hosting has its own unique SFTP connection details:

1. Log in to your server on the panel at [panel.vellix.host](https://panel.vellix.host).
2. Click on the **"Settings"** or **"SFTP"** tab in the sidebar navigation menu.
3. Locate the **SFTP Details** section to find:
   * **Server Address / Host:** The address of the node hosting your server (e.g., `sftp.vellix.host` or an IP address).
   * **Port:** Usually `2022` (the standard SFTP port for our panel daemon).
   * **Username:** A unique user identifier formatted as `yourusername.serverid` (e.g., `admin.a1b2c3d4`).
   * **Password:** **This is the exact same password** you use to log in to the web panel dashboard.

---

2. ## Connecting with FileZilla (Recommended)

[FileZilla](https://filezilla-project.org/) is a free, cross-platform SFTP client available for Windows, macOS, and Linux.

### Steps to connect:
1. Launch FileZilla.
2. In the **Quickconnect** bar at the top, fill in the following fields:
   * **Host:** Copy and paste the *Server Address* from the panel.
   * **Username:** Copy and paste the *Username* from the panel.
   * **Password:** Enter your account password.
   * **Port:** Enter `2022`.
3. Click the **"Quickconnect"** button.
4. If a warning prompt about an *"Unknown host key"* appears, check the box *"Always trust this host"* and click **OK**.
5. Once connected, your computer's local files will show on the left, and your remote server directory will appear on the right. You can now drag and drop files to transfer them.

---

3. ## Connecting with WinSCP (Windows Only)

[WinSCP](https://winscp.net/) is a popular, free Windows-only utility for secure transfers.

### Steps to connect:
1. Open WinSCP.
2. In the **Login** window, configure the following:
   * **File protocol:** Select **SFTP**.
   * **Host name:** Enter the *Server Address* from the panel.
   * **Port number:** Enter `2022`.
   * **User name:** Enter your *Username* from the panel.
   * **Password:** Enter your account password.
3. Click **"Login"** (or click **"Save"** to store this session for easier future access).
4. Accept the server host key warning on your first connection.

---

## Essential Transfer Tips

> [!TIP]
> **Avoid transferring raw folders with thousands of tiny files:** Protocols like SFTP require a handshake for every single file. Transferring a folder with 2,000 mod files directly can take hours. Instead, zip the folder on your computer, upload the single `.zip` file via SFTP, and then use the web file manager's **"Unarchive"** option to extract it in seconds.

> [!WARNING]
> If you update your account password on the web panel (as described in the Security guide), your SFTP password updates instantly to match it. Don't forget to update your saved connection passwords in FileZilla or WinSCP!
