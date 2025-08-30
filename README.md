# tml-debug-quickstart
Skip the splash screen and character / world select menus when debugging your Terraria mods

## READ FIRST
These files are used to make debugging Terraria mods with Visual Studio faster. This only works if you rebuild your mod from Visual Studio rather than ingame. Please don't build ingame 😘
<hr>

## Usage Guide
### Download files
Download the 2 root files (`Program.cs` and `SkipSplashScreen.cs`) and import them into your mod project. This will skip the beginning splash screen when starting a debug session, saving countless seconds over many restarts and making your workflow blazingly fast 🔥
<br>
<br>

### Replace `launchSettings.json`
Replace your mod project's auto-generated `Properties/launchSettings.json` file with the one in this repository. This will create a new launch option that, on top of utilizing the splash screen skip, skips the player and world selection screens.
<br>
<br>

### Change Launch Profile
Your launch profile can be found near the top of the screen. Click the dropdown arrow to see all available profiles and select the one named `Terraria (hot reload+ watcher)`

<img width="289" height="99" alt="image" src="https://github.com/user-attachments/assets/45f9ccda-5837-4724-bc33-95af700a7ab4" />
<br>
<img width="270" height="130" alt="image" src="https://github.com/user-attachments/assets/afc42b04-5497-4cce-bbf2-8f5353df576f" />
<br>
<br>

### And that's it!
Now when you click that profile or press F5 to start a new debugging session, the game will skip the splash screen, player select, and world select, so you can test your mod as quickly as possible.
<br>
<br>

### Specify launch arguments (optional extra step)
In the new `launchSettings.json` file, you will see a launch argument called `-skipselect`.

By default, this selects the first player and world from each list. To specify a player or world by name, add to the argument like so:

```
"commandLineArgs": "\"$(TerrariaSteamPath)$(tMLPath)\" -skipselect \"Player Name:World Name\""
```

You can omit either one to use its default option, e.g. `-skipselect \"Player Name\"` or `-skipselect \":World Name\"`.
<br>
<br>
