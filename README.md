# P6 Clones Timing

An Alt1 plugin for RuneScape 3 that detects the P6 clone spawn message and displays an overlay timer to help you execute your rotation.

## Installation

Click the link below or paste it into your browser:

```
alt1://addapp/https://nullopt.github.io/appconfig.json
```

Or manually add in Alt1:
1. Open Alt1's browser (globe icon)
2. Navigate to `https://nullopt.github.io/appconfig.json`
3. Click "Add App"

## Features

### Combat Styles

**Magic Mode**
- Single 6-second countdown timer
- Shows when to use your next ability after clones spawn

**Necro Mode**  
- Sequential ability rotation with individual timers:
  - Invoke Death (2.4s)
  - Threads of Fate (1.8s)
  - Bloat (1.8s)
  - Volley of Souls (1.8s)
  - T90 Spec + EOF (1.8s)

### Settings

- **Combat Style** - Switch between Magic and Necro rotations
- **Show ticks** - Display time in 0.6s tick intervals instead of whole seconds
- **Show image** - Toggle ability icons in the overlay
- **Show progress bar** - Toggle the countdown progress bar
- **Debug console** - Show detailed logs for troubleshooting

All settings are saved automatically.

## How It Works

1. The plugin reads your chatbox for the trigger phrase
2. When "I WILL NOT BE SUBJUGATED BY A MORTAL!" appears, the timer starts
3. Follow the overlay countdown to execute your rotation

## Requirements

- [Alt1 Toolkit](https://runeapps.org/alt1)
- RuneScape 3 in compatibility mode or windowed

## Permissions

This plugin requires:
- **Pixel** - To read the chatbox
- **Overlay** - To display the timer on screen
- **Game State** - To detect game window position

## Resources

- [Alt1 Toolkit](https://runeapps.org/alt1)
- [GitHub Repository](https://github.com/nullopt/P6ClonesTiming)
