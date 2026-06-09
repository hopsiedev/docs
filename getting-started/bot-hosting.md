---
title: "Discord Bot Hosting"
sidebarTitle: "Bot Hosting"
description: "Learn how to host and create free Discord bot servers at Vellix Hosting"
---

Vellix Hosting offers free Discord bot hosting through our Discord community integration. Follow this guide to set up, deploy, and configure your Node.js application.

---

## Service Specifications

When you create a free Discord bot server, you get:

* **Dedicated Runtime**: Isolated Node.js environment in a Docker container.
* **Memory (RAM)**: 250 MB RAM.
* **Storage**: 1 GB High-Speed SSD storage.
* **Management**: Full console access and FTP/SFTP file management.

---

## Step-by-Step Hosting Guide

Follow these steps to deploy your bot:

### 1. Create Your Server
Join our Discord server and navigate to the dedicated ticket or bot channel:
* **Discord Channel**: [Join Discord Support](https://discord.com/channels/1504707289385533461/1512867928717000876)
* Click the server creation button.
* ⚠️ **Important**: Make sure your Discord Direct Messages (DMs) are open so our bot can send you your temporary panel password!

### 2. Log In to the Panel
* Access the control panel: [panel.vellix.host](https://panel.vellix.host)
* Log in using your email address and the temporary password sent to your Discord DMs.
* (Optional) We recommend updating your password in the account settings immediately.

### 3. Upload Your Bot Files
* Select your newly created server from the dashboard.
* Go to the **File Manager** tab in the sidebar.
* Upload your bot code files (e.g., `index.js`, `package.json`, `.env` files).
* > [!CAUTION]
  > **Do NOT upload the `node_modules` directory.** The panel will install dependencies automatically to save bandwidth and storage.

### 4. Install Dependencies
* Go to the **Console** tab.
* Your packages will be installed automatically from your `package.json` when you first start the server, or you can specify custom startup options.

### 5. Start Your Bot
* Configure your environment variables, token, and secrets on the panel.
* Click the green **Start** button in the Console to boot your bot!
