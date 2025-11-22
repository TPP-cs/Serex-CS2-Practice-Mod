# Serex-CS2-Practice-Mod
<img width="1280" height="720" alt="practicemodv1" src="https://github.com/user-attachments/assets/15e84bfd-4fe0-4ead-b505-8324fe5b793b" />
Serex's CS2 Practice Mod is a custom game mode designed for self-hosted cs2 servers, it requires metamod and css! The plugin provides more than 30 relevant practice commands, memory for grenade lineups, bot management, run boost practice and much more! Available on both linux &amp; windows servers for offline&amp;online use!

## ⚡️ Features

### 🌪 Practice:
- **Grenade Practice**: Unlimited grenades, trajectory visualization, throw stats
- **Rethrow System**: Return to last throw position or rethrow the grenade
- **Save/Load Positions**: Save unlimited grenade lineups 
- **Noclip & God Mode**: Fly around and practice invincible
- **Spawn Browsing**: Cycle through T/CT spawns
- **Flash Immunity**: Makes the effect minimal (Searching for someone who knows how to change color)
- **Damage Stats**: Track grenade damage and reset when needed

### 🐀 Bots:
- **Add Bots**: Smart team balancing
- **Place Bots**: Position bots at your position
- **Bot Control**: Make bots crouch/stand/jump
- **Remove Bots**: Aim at bot an remove individually or remove all at once
- **Auto-Respawn**: Bots respawn at death/place location after 3 seconds
- **Run Boost**: Teammate bots follow you for run boosts!

### 🛠️ Utility:
- **Clear**: Remove all grenades and effects
- **Impacts**: Toggle bullet impact markers
- **Restart**: Restart the round
- **Map Change**: Change map
- **GO/TP**: Teleport to coordinates

## 🗿 Requirements:

- **CS2 Dedicated Server** (Windows or Linux)
- **Metamod** (v2.0+)
- **CounterStrikeSharp** (v1.0.347)

## 📥 Quick Start:

See [INSTALLATION.md](INSTALLATION.md) for detailed setup instructions.

## 💬 Command List:

### Practice Commands
| Command | Aliases | Description |
|---------|---------|-------------|
| `!practice` | `!prac` | Toggle practice mode |
| `!help` | `!phelp` | Show command list |
| `!back` | `!rethrow` | Return to last throw position |
| `!savenade <name>` | - | Save current position |
| `!loadnade <#>` | - | Load saved position |
| `!listnades` | - | List all saved positions |
| `!deletenade <#>` | `!delnade` | Delete saved position |
| `!thrownade <#>` | - | Load position and give grenade |
| `!noclip` | - | Toggle fly mode |
| `!god` | - | Toggle invincibility |
| `!clear` | - | Clear grenades and smokes |
| `!impacts` | - | Toggle bullet impacts |
| `!go <x, y, z>` | `!goto` | Teleport to coordinates |
| `!tspawn [#]` | - | Browse T spawn points |
| `!ctspawn [#]` | - | Browse CT spawn points |
| `!map <name>` | - | Change map |
| `!noflash` | `!flash` | Toggle flash immunity |
| `!restart` | `!reset` | Restart the round |
| `!damage` | `!stats` | Show grenade damage stats |
| `!clearstats` | - | Clear damage stats |

### Bot Commands
| Command | Aliases | Description |
|---------|---------|-------------|
| `!bot` | - | Add a bot (auto-balances teams) |
| `!ctbot` | - | Add a CT bot |
| `!tbot` | - | Add a T bot |
| `!nobot` | `!removebot` | Remove bot you're aiming at |
| `!kickbots` | `!nobots` | Remove all bots |
| `!place` | `!placebot` | Place bot at your position |
| `!boost` | `!duck`, `!crouch` | Make all bots crouch |
| `!stand` | - | Make all bots stand |
| `!jump` | - | Make closest bot jump |

## 🔮 Tips:

### Bind Commands
Use any command with `bind K css_name` for example css_boost
will make the bots crouch when "K" is pressed, you can bind
all your favorite and most used commands to keys for faster use!

### Saving Grenade Lineups
1. Position yourself for the throw
2. Use `!savenade <name>` (e.g., `!savenade mirage_a_smoke`)
3. Your position, angle, and current grenade are saved
4. Use `!listnades` to see all saved positions
5. Use `!loadnade 1` to return to that lineup

### Run Boost Practice
1. Add a teammate bot: `!ctbot` (or `!tbot`)
2. Place bot: `!place`
3. Make bot crouch: `!boost`
4. Jump on bot's head and run forward
5. Jump off for realistic run boost momentum!

### Grenade Practice
- All grenades auto-refill
- Throw stats show airtime and distance
- Use `!back` to quickly retry throws
- `!damage` shows total damage dealt

## 🐛 Known Issues:

- Run boosting with bots may get the bot stuck underground
- Run boost only works on teammate bots
- Bot crouch/stand affects ALL bots globally

## 👁 Credits:
**Author**: Serex

**Version**: 1.1.0

*Compatible with latest CS2 updates*

## ⛔️ License:

Free to use and modify for personal and community servers.

---

**Have fun practicing! ♻️🔫**
