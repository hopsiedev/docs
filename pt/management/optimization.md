# Server Optimization & Performance Tips

Lag and rubber-banding can ruin the player experience. While Vellix Hosting provides high-frequency Ryzen 9 processors and fast NVMe SSDs, unoptimized server software, heavy mod configurations, or excessive entity counts can still degrade performance.

Follow these professional optimization tips to keep your server running at a solid 20 TPS (Ticks Per Second).

---

## 1. Pre-Generate Your World (Critical for Minecraft)

Generating new chunks on-the-fly when players fly around with Elytras or run fast is the #1 cause of server lag. It stresses both the CPU and disk read/write cycles.

### How to pre-generate chunks:
1. Install the **Chunky** plugin (compatible with Spigot, Paper, Fabric, Forge).
2. Stop your server.
3. In `server.properties`, set your world border size (e.g., a radius of 5,000 blocks).
4. Start the server and run these commands in the **Console**:
   * `chunky center 0 0` (sets the generation center).
   * `chunky radius 5000` (sets the generation radius).
   * `chunky start` (starts the generation process).
5. Let Chunky complete the task before allowing players to join. It may take several hours depending on the radius. Once finished, chunk loading lag will be virtually eliminated.

---

2. ## Optimize Server Configuration Files

If you are running a Minecraft server, use **Paper** or **Purpur** instead of Vanilla or Spigot. They contain advanced performance patches.

Open the following files in the **Web File Manager** and adjust these values:

### `server.properties`
* `view-distance=6` (Controls how many chunks are sent to the client. Values between 6 and 8 are recommended).
* `simulation-distance=4` (Controls which chunks active entities and ticks run in. Lowering this to 4 or 5 drastically reduces CPU load).

### `paper-world-defaults.yml` (or `spigot.yml`)
* **Entity activation ranges:** Lower the distance at which animals, monsters, and miscellaneous items tick.
* **Max entity collisions:** Limit how many times entities check for collisions per tick (e.g., set `max-entity-collisions=2`).

---

3. ## Garbage Collection & Memory Tips

* **Use Modern Java Versions:** Newer Java versions (like Java 21) have superior garbage collection (ZGC / G1GC) that reduces lag spikes during memory cleanup.
* **Avoid Bloated Modpacks:** Each active mod increases memory footprint. Remove aesthetic-only mods that aren't critical to gameplay, or mods that perform excessive ticking calculations.
* **Monitor Logs for Spam:** If a plugin is throwing errors in your Console constantly, it will write thousands of lines to your disk, creating disk lag. Repair the configuration or remove the faulty plugin.
