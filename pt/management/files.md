# Web File Manager

The **File Manager** (found under the **Files** tab in the sidebar menu) allows you to manage all your server data directly from your web browser without requiring external software.

---

## Basic File Operations

When you open the File Manager, you will see your server's root directory. From here, you can perform several core actions:

* **Create Files & Folders:** Click the **"Create File"** or **"New Folder"** buttons in the upper-right corner.
* **Edit Files:** Click on any text-based file (such as `.yml`, `.json`, `.conf`, `.properties`, or `.txt`). This opens an **integrated code editor** with syntax highlighting. After making your changes, click **"Save Content"** at the bottom.
* **Upload Files:** Drag and drop files from your computer directly into the browser window, or click the **"Upload"** button to browse and select files.
  > [!TIP]
  > The web file manager is perfect for individual configuration edits or uploading smaller files (under 100 MB). For larger transfers (such as entire maps, worlds, or large modpacks), we recommend connecting via **SFTP**.

---

## Action Menu (The Three Dots `...`)

To the right of each file and folder, you will find a three-dot button `...` that opens the action menu:

1. **Rename:** Change the name of a file or directory.
2. **Move / Copy:** Relocate the file. You can move files by providing their relative path (e.g., move `server.properties` into a folder by inputting `backup-configs/server.properties`).
3. **Download:** Save the file directly onto your computer.
4. **Delete:** Permanently remove the file or folder from the server storage.
   > [!WARNING]
   > Deleting files is permanent and cannot be undone. Create a backup of your server before performing bulk deletions.

---

## Compressing & Extracting Archives (.zip)

Uploading folders containing hundreds of individual small files (such as modpacks or plugin configurations) one-by-one is highly inefficient. Instead:

1. Compress the folder on your computer into a `.zip` archive.
2. Upload the single `.zip` file to the panel (via the Web File Manager or SFTP).
3. In the Web File Manager, click the three dots `...` next to the uploaded `.zip` file.
4. Select **"Unarchive"** or **"Decompress"**. The panel will extract all files and subfolders instantly.
5. *(Optional)* Delete the uploaded `.zip` file to save disk space.

You can also compress files on the panel by selecting them using the checkboxes on the left, clicking the **"Archive"** button at the top, and downloading the resulting `.zip` file.
