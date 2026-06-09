# Uploading & Installing Mods/Plugins

Customizing your server with mods, plugins, or custom game modes is one of the best ways to enhance the gameplay experience. This guide will walk you through installing individual plugins, mods, and entire server modpacks on your Vellix Hosting server.

---

## 1. Plugins vs. Mods: Which does my server use?

Before uploading files, you must know what your server software supports:
* **Plugins (Spigot, Paper, Purpur):** Extend server functionality (like adding claims, economy, or chat prefixes) without requiring players to install anything on their computers.
* **Mods (Forge, Fabric, NeoForge):** Add custom blocks, items, creatures, and dimensions. **Both the server and the players must have the exact same mods installed.**

---

## 2. Installing Individual Plugins or Mods

1. Download the `.jar` files for the plugins/mods you want to use from trusted sources (e.g., CurseForge, Modrinth, or SpigotMC).
   * *Make sure they are compatible with the game version your server is running.*
2. Stop your server from the **Console**.
3. Open the **Web File Manager** or connect via **SFTP**.
4. Navigate to the appropriate folder:
   * For Spigot/Paper/Purpur plugins: Upload the `.jar` files to the **`plugins/`** directory.
   * For Forge/Fabric mods: Upload the `.jar` files to the **`mods/`** directory.
5. Go back to the **Console** and click **Start** or **Restart**.
6. Verify they loaded correctly:
   * In Minecraft, run the command `plugins` in the console (or `/plugins` in-game) to see your active plugins.

---

## 3. Installing a Complete Modpack (e.g., CurseForge server pack)

To run a pre-packaged modpack (like RLCraft, Pixelmon, or Better MC):

1. Download the **Server Pack** files for the modpack (usually a `.zip` archive containing the `mods`, `config`, and libraries folders).
2. Stop your server.
3. Open your **SFTP** client and connect to the server.
4. If you have existing files, you should back them up first, then delete them from the server directory to avoid conflicts.
5. Upload the modpack `.zip` archive to the root directory of your server.
6. Open the **Web File Manager** in your browser, locate the uploaded `.zip` file, click the three dots `...` and choose **"Unarchive"** to extract all files.
7. Verify the startup settings:
   * Under the **"Startup"** tab in the sidebar, ensure you have selected the correct **Java Version** required by the modpack (e.g., Java 17 for Minecraft 1.18+, Java 21 for Minecraft 1.20.5+).
   * Ensure the **Server Jar File** or startup parameters match the modpack launch script requirements.
8. Go back to the **Console** and click **Start**.

---

## Troubleshooting Common Issues

* **Server is stuck in a boot loop:** Check the console log. If you see `java.lang.UnsupportedClassVersionError`, it means your Java version is outdated or too new for your game version. Change the Java version in the **Startup** tab.
* **Missing dependency error:** Some mods or plugins require other core library mods to work. Read the mod/plugin description page and upload the missing dependencies to your server folder.
* **Modpack not loading custom blocks:** Check that you uploaded the mod files to the server's `mods/` directory, and that you have installed the exact same modpack version on your local launcher (CurseForge App, Modrinth App, Prism Launcher).
