You are a Minecraft plugin developer specialized in Spigot 1.20–1.21 plugins.

I’m building an advanced anticheat plugin called **WitherAC** for my Minecraft SMP.  
The plugin must detect and prevent these hacks using real in-game logic and Bukkit API:

1. Fly
2. Speed
3. Jump (double jump/multi-jump)
4. Jesus (walking on water detection — ignore swimming, elytra, dolphins grace, potions, tridents)
5. NoFall
6. AutoClicker (CPS detection with jitter tolerance)
7. KillAura (angle + reach + switch)
8. Timer (tick-speed or movement anomaly)
9. Unauthorized Access (Force OP / Creative mode / GameMode switch abuse / Should able to revert gamemode or op)

**Plugin details:**
- Name: `WitherAC`
- Main class: `com.witherac.WitherAC`
- Language: Java 21 (Spigot API)
- Use `ViolationManager`, `BanManager`, and `DiscordNotifier` and other classes.
- Each detector should implement `Listener` and use `ViolationManager.addViolation(player, amount, reason)`.
- Violations decay over time (configurable).
- Discord webhook integration to log detections.
- Auto-ban/kick thresholds and color-coded messages.
- Config file should include detailed thresholds and options for each detector.
- Add `/wac` command to manage bans, view violations, and reload config.
- Include safe event handling (ignore spectators, vanished players, potions , elytras,creative mode, etc.)
- Use Bukkit scheduler for timing logic.
- Generate the full folder structure and code for all classes.

Now — generate:
1. All Java source files (main, managers, detectors, commands).
2. `plugin.yml` file.
3. `config.yml` file with proper formatting and color support.

Ensure:
- No syntax or import errors.
- Fully compatible with Java 21 and Spigot 1.20.6+.
- Logic prioritizes **false-positive/negative prevention**.
- Water-walking (Jesus) detector must check the player’s block positions accurately and ignore swimming or potion effects.

Generate everything cleanly.
