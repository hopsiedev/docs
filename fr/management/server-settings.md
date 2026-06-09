# Startup Options & Port Allocations

To run custom mods, configure voting systems, set up voice chats, or modify the version of Java your server runs, you will need to manage your port allocations and startup variables.

---

## 1. Port Allocations (Network Settings)

Your server is assigned a primary IP and port (e.g., `190.22.44.112:25565`). Some plugins (such as *Dynmap*, *Votifier*, or *Simple Voice Chat*) require their own additional ports to communicate.

### How to request and assign additional ports:
1. Log in to [panel.vellix.host](https://panel.vellix.host) and select your server.
2. Click on the **"Network"** tab in the sidebar menu.
3. If you have available allocations, click **"Create Allocation"** (or open a support ticket on Discord if you need additional ports assigned to your node).
4. The new port will appear in the list.
5. In your plugin configuration file, replace the default port with your new assigned port (never use random ports; only use ports specifically allocated to your server in the Network tab).

---

2. ## Modifying Startup Options

The **"Startup"** tab contains key environment variables that determine how the game server executable is launched:

* **Java Version:** Select the Java development kit (JDK) version.
  * **Java 8 / 11:** For older Minecraft versions (1.12.2 and below).
  * **Java 17:** Standard for Minecraft 1.18 through 1.20.4.
  * **Java 21:** Standard for Minecraft 1.20.5 and above.
* **Server Jar File:** The name of the file the server will run (e.g., `server.jar` or `vanilla.jar`). Make sure the file uploaded in your File Manager has the exact same name as the one entered here.
* **Startup Command Variables:** Custom flags such as max players, query ports, or server versions depending on the game.

> [!IMPORTANT]
> Some startup variables are locked by the system to maintain stability. If you need to make modifications to locked fields or need custom startup flags (such as Aikar's Flags for performance), contact our support team in Discord.
