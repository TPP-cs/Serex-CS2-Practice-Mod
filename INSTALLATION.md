# ⚙️ Installation Guide - Serex CS2 Practice Mod

Complete step-by-step installation guide for the plugin.

## 🗿 Requirements:

Before installing, ensure you have:

1. **CS2 Dedicated Server** (Windows or Linux)
   - Download: https://developer.valvesoftware.com/wiki/SteamCMD
   - Installed and running
   - Admin/FTP access to server files

3. **Metamod:Source** (v2.0 or higher)
   - Download: https://www.sourcemm.net/downloads.php?branch=master
   - Required for CounterStrikeSharp&PracticePlugin

4. **CounterStrikeSharp** (v1.0.347 or higher)
   - Download: https://github.com/roflmuffin/CounterStrikeSharp/releases
   - Framework for CS2 plugins  

---

## ✔️ Step 1: Install Metamod

### Windows Server:
1. Download Metamod for Windows
2. Extract the `addons` folder to your CS2 server directory:
```
   C:\GameServers\CS2\game\csgo\
```

### Linux Server:
1. Download Metamod for Linux
2. Extract the `addons` folder to your CS2 server directory:
```
   /home/steam/cs2/game/csgo/
```

In game\csgo update gameinfo.gi to include `Game    csgo/addons/metamod` under "SearchPaths"

### Verify Installation:
1. Start your CS2 server
2. Type `meta version` in server console
3. You should see Metamod version information

---

## ✔️ Step 2: Install CounterStrikeSharp

1. **Download CounterStrikeSharp** from releases page
2. **Extract** the downloaded archive
3. **Copy** the entire `addons` and `gameinfo.gi` files to:
```
   YourServer/game/csgo/
```
4. **Merge** with existing folders if prompted

### Verify Installation:
1. Restart your CS2 server
2. Type `css_plugins list` in console
3. You should see CounterStrikeSharp loaded

---

## ✔️ Step 3: Install Practice Mod Plugin

### Automatic Installation (Recommended):

1. **Download** `PracticeMod-vX.X.X.zip`
2. **Extract** the archive
3. **Copy** the `addons` folder to your server:
```
   YourServer/game/csgo/
```
4. **Merge** with existing folders when prompted

### Manual Installation:

1. Navigate to:
```
   YourServer/game/csgo/addons/counterstrikesharp/plugins/
```
2. Create folder: `PracticeMod`
3. Copy `PracticeMod.dll` into this folder

### Final Structure:
```
csgo/
├── addons/
│   ├── metamod/
│   │   └── (Metamod files)
│   └── counterstrikesharp/
│       ├── (CSS core files)
│       └── plugins/
│           └── PracticeMod/
│               ├── PracticeMod.dll
└── cfg/
    └── practice.cfg (optional)
```

---

## ⚠️ Step 4: Configure Server (Optional)

### Create practice.cfg (optional):

Create `csgo/cfg/practice.cfg`:
```cfg
// Practice Mod Server Config
hostname "Practice Server"
sv_lan 0
sv_cheats 1

// Ensure these are set
mp_warmup_end
mp_restartgame 1

echo "Practice config loaded!"
```

### Load on Server Start:

Add to `server.cfg` or `autoexec.cfg`:
```cfg
exec practice.cfg
```

---

## ✅ Step 5: Verify Installation

1. **Start/Restart** your CS2 server

2. **Check console** for:
```
   [PracticeMod] vX.X.X loaded!
```

3. **Connect to server** and type in chat:
```
   !practice
```

4. **You should see**:
```
   [Practice] Practice mod ENABLED!
   [Practice] Type !help for commands
```

---

## ⁉️ Step 6: Usage

### Enable Practice Mod:
```
!practice
```

### See All Commands:
```
!help
```

### Test Bot Features:
```
!bot        // Add a bot
!place      // Place bot at your location
!boost      // Make bots crouch
```

### Test Grenade Features:
```
// Throw a grenade
!back       // Return to throw position
!savenade test    // Save the position
!listnades  // View saved positions
```

---

## 🐛 Troubleshooting

### Plugin Not Loading:

**Problem**: No `[SPracticeMod]` message in console

**Solutions**:
1. Verify CounterStrikeSharp is installed: `css_plugins list`
2. Check plugin path: `csgo/addons/counterstrikesharp/plugins/PracticeMod/`
3. Ensure `PracticeMod.dll` exists in the folder
4. Check server console for error messages
5. Verify .NET 8.0 Runtime is installed on server

### Commands Not Working:

**Problem**: Typing `!practice` does nothing

**Solutions**:
1. Ensure practice mod is enabled: `!practice`
2. Check you're not a spectator
3. Verify plugin loaded: `css_plugins list`
4. Try alternative command: `!prac`

### Bots Not Spawning:

**Problem**: `!bot` says "No bots available"

**Solutions**:
1. Ensure practice mod is enabled
2. Check server console for errors
3. Try: `bot_quota 0` then `!bot` again
4. Verify bot commands work: `bot_add` in console

### Performance Issues:

**Problem**: Server lag with plugin

**Solutions**:
1. Ensure server has adequate resources
2. Check for conflicting plugins
3. Monitor server CPU/RAM usage

---

## 🔄 Updating the Plugin

1. **Backup** your current `SPracticeMod` folder
2. **Backup** saved grenade positions:
```
   csgo/addons/counterstrikesharp/plugins/PracticeMod/nades_*.json
```
3. **Stop** the server
4. **Replace** `SPracticeMod.dll` with new version
5. **Start** the server
6. **Verify** version in console

---

## 📞 Support

### Common Issues:

- **Plugin won't load**: Ensure newest CSS is installed
- **Commands not working**: Practice mod must be enabled first
- **Bots won't spawn**: Check server bot settings aren't conflicting
- **Grenades not refilling**: Ensure `sv_infinite_ammo 2` is set
- **Ensure you have added `Game    csgo/addons/metamod` in gameinfo.gi**

### Getting Help:

1. Check console for error messages
2. Verify all requirements are installed
3. Test on a fresh server if possible
4. Check CounterStrikeSharp compatibility

---

## 📦 Complete File Checklist

Before running, verify you have:

- ✅ Metamod:Source installed
- ✅ CounterStrikeSharp installed
- ✅ `PracticeMod.dll` in correct folder
- ✅ Server restarted after installation
- ✅ Plugin shows in `css_plugins list`
- ✅ `!practice` command works in-game

---


**Installation complete! Enjoy your practice server! ♻️🔫**
