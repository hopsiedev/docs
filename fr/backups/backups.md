# Backups & Restoration

Protecting your server progress is crucial. Data loss can happen due to malfunctioning mods, corrupted save files, or configuration errors. In this guide, you will learn how to create manual backups, restore them, and schedule automatic backups.

---

## 1. Creating a Manual Backup

You should always create a backup before making major changes, updating game versions, or adding new mods.

1. Go to your server on the panel at [panel.vellix.host](https://panel.vellix.host).
2. Click on the **"Backups"** tab in the sidebar menu.
3. Click the **"Create Backup"** button in the upper-right corner.
4. Fill out the fields:
   * **Backup Name:** Give your backup a descriptive name (e.g., *Before forge update* or *World save 2026*).
   * **Ignored Files & Folders:** *(Optional)* Enter relative paths to files or folders you want to exclude from the backup (e.g., excluding the `backups/` folder itself, or large logs like `logs/` to save space). Each rule must go on a new line.
5. Click **"Start Backup"**.

The panel will pack your files into a secure archive in the background. The backup card will show a spinner until it is fully completed.

---

## 2. Restoring or Downloading a Backup

Once a backup is created, click the three dots `...` on the backup card to open the action menu:

* **Restore:** Reverts all server files to the state they were in when the backup was taken.
  > [!WARNING]
  > **Restoring a backup will overwrite existing files.** You can check the box *"Delete files before restoring"* to clean the server directory and ensure no old, conflicting files remain before placing the backup files.
* **Download:** Downloads the backup archive (`.tar.gz`) directly to your computer.
* **Lock / Unlock:** Locking a backup prevents it from being deleted automatically or manually by mistake when you hit your backup limit.
* **Delete:** Permanently deletes the backup archive to free up space.

---

## 3. Scheduling Automatic Backups

Creating backups manually is helpful, but automating the process ensures you never lose progress even if you forget to run them. You can configure a backup schedule under the **"Schedules"** tab:

1. Click on the **"Schedules"** tab in the sidebar.
2. Click **"Create Schedule"** in the upper-right.
3. Name your schedule (e.g., *Daily Backup*).
4. Set the frequency using Cron notation. Here are common presets:
   * **Every Day at Midnight:** Minutes: `0`, Hours: `0`, Day of month: `*`, Month: `*`, Day of week: `*`
   * **Every 12 Hours:** Minutes: `0`, Hours: `*/12`, Day of month: `*`, Month: `*`, Day of week: `*`
5. Click **"Create Schedule"**.
6. Click on the newly created schedule in the list, then click **"New Task"** at the top right.
7. Change the **Action** to **"Create Backup"**.
8. Fill in the ignored files (if any) and click **"Create Task"**.

Your server will now run automatic backups at the configured interval.
