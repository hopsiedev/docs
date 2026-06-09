# Console & Power Controls

The **Console** is the primary interface for interacting directly with your game server. In this guide, you will learn how to monitor hardware usage, send game commands, and manage your server's power states.

---

## Power Controls (Action Buttons)

In the upper-right corner or sidebar of the Console dashboard, you will find four main power control buttons:

* **Start:** Powers on the server container and launches the game process. Use this if your server is currently "Offline".
* **Stop:** Sends a graceful shutdown signal to the game (e.g., executing `/stop` or `/save-all` in Minecraft). This saves your progress and safely shuts down the server.
* **Restart:** Gracefully stops the game and boots it back up immediately. Ideal for applying configuration changes or clearing RAM cache.
* **Kill:** Instantly terminates the game process without saving.
  > [!CAUTION]
  > **Only use "Kill" if your server is completely frozen or unresponsive to the "Stop" command.** Using Kill regularly can cause file corruption, rollback your world progress, or corrupt database entries.

---

## Real-Time Monitoring Graphs

The Reviactyl panel displays continuous, real-time graphs representing your server's resource utilization:

1. **CPU Usage:** The percentage of processing power being used. If it remains near 100% for long periods, players may experience lag (consider optimizing plugins, mods, or upgrading your plan).
2. **Memory Usage (RAM):** Displays the current memory allocated compared to your plan limit (e.g., `4 GB / 8 GB`).
   * *If the server exceeds its memory limit, the panel's built-in OOM (Out Of Memory) killer will automatically stop the server to protect node stability. Optimize your game files or upgrade your plan if you hit this limit frequently.*
3. **Disk Usage:** Total storage space consumed by your game files (mods, worlds, logs, backups). Make sure to delete old log files (`latest.log`, `debug.log`) or old backups to free up disk space.

---

## Sending Console Commands

Below the live black terminal screen, there is a text command bar labeled **"Type a command..."**:

* You can type any command here to control the game directly from the console without needing in-game administrator privileges.
* **Do not prefix commands with a slash (`/`)**. For example, type `op PlayerName` or `say Hello World` and press Enter.
* Any responses or errors from the game server will print in real-time on the console log above.
