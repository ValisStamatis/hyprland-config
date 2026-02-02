# Hyprland Dotfiles

A comprehensive Hyprland configuration setup with custom themes, animations, shaders, and workflows, based on the [HyDE](https://github.com/HyDE-Project/HyDE) framework.

## Overview

This repository contains my personal Hyprland dotfiles, built upon the HyDE (Hyprland Desktop Environment) framework, featuring:

- **Hyprland**: Wayland compositor configuration
- **Hypridle**: Idle management and screen locking
- **Hyprlock**: Lockscreen with custom themes
- **Pyprland**: Plugin system with scratchpads
- **HyDE Framework**: Theme management and configuration system
- **Custom Themes**: Catppuccin Mocha GTK theme with Dracula icons
- **Animations**: Multiple animation presets
- **Shaders**: Various screen effects (blue light filter, grayscale, etc.)
- **Workflows**: Different configurations for gaming, editing, etc.

## Dependencies

### Core Hyprland Ecosystem

- `hyprland` - The Wayland compositor
- `hypridle` - Idle management daemon
- `hyprlock` - Screen locker
- `pyprland` - Plugin system for Hyprland

### Applications

- `kitty` - Terminal emulator
- `nemo` - File manager
- `rofi` - Application launcher and menu
- `waybar` - Status bar
- `swaync` - Notification daemon
- `grim` - Screenshot tool
- `slurp` - Screen area selector
- `wl-clipboard` - Wayland clipboard utilities

### System Utilities

- `pipewire` - Audio system (provides `wpctl`)
- `brightnessctl` - Screen brightness control
- `playerctl` - Media player control
- `network-manager-applet` - Network management
- `xdg-desktop-portal-hyprland` - Desktop portal for Hyprland

### Themes

- GTK Theme: `catppuccin-mocha`
- Icon Theme: `tela-circle-dracula`

### Additional Tools

- `hyde` - Custom theme and configuration manager (includes `hyde-shell`)
- Hyde Framework: [HyDE Project](https://github.com/HyDE-Project/HyDE)

## Installation

1. **Install Hyprland and dependencies:**

   ```bash
   # On Arch Linux
   sudo pacman -S hyprland hypridle hyprlock pyprland kitty nemo rofi waybar swaync grim slurp wl-clipboard pipewire brightnessctl playerctl network-manager-applet xdg-desktop-portal-hyprland

   # Install themes
   # GTK theme (Catppuccin-Mocha)
   # Icon theme (Tela-circle-dracula)
   ```

2. **Clone this repository:**

   ```bash
   git clone https://github.com/yourusername/hyprland-dotfiles.git ~/.config/hypr
   ```

3. **Install Hyde:**
   - Clone and install the [HyDE framework](https://github.com/HyDE-Project/HyDE)
   - Follow the official installation guide for your distribution

4. **Copy configurations:**

   ```bash
   cp -r hypr/* ~/.config/hypr/
   ```

5. **Set themes:**
   - Configure GTK theme to Catppuccin-Mocha
   - Configure icon theme to Tela-circle-dracula
   - Set color scheme to prefer-dark

## Keybindings

### Window Management

- `Super + Q` - Open terminal (Kitty)
- `Super + F` - Open file manager (Nemo)
- `Super + R` - Open menu (Rofi)
- `Super + D` - Application launcher (Rofi drun)

### Media Controls

- `XF86AudioRaiseVolume` - Increase volume
- `XF86AudioLowerVolume` - Decrease volume
- `XF86AudioMute` - Toggle mute
- `XF86AudioMicMute` - Toggle microphone mute
- `XF86AudioPlay/Pause` - Play/pause media
- `XF86AudioNext/Prev` - Next/previous track

### System Controls

- `XF86MonBrightnessUp/Down` - Adjust brightness
- `Super + S` - Take screenshot (saved to ~/Pictures/Screenshots/)

## Features

### Animations

Multiple animation configurations available in `animations/`:

- `classic.conf` - Classic animations
- `fast.conf` - Fast animations
- `minimal.conf` - Minimal animations
- And many more...

### Shaders

Screen effects in `shaders/`:

- `blue-light-filter.frag` - Blue light reduction
- `grayscale.frag` - Monochrome display
- `invert-colors.frag` - Color inversion
- `oled-saver.frag` - OLED screen protection
- And more...

### Workflows

Different configurations for various use cases in `workflows/`:

- `default.conf` - Standard configuration
- `editing.conf` - Optimized for writing/editing (disables blur for better contrast)
- `gaming.conf` - Gaming optimized
- `powersaver.conf` - Power saving mode

### Themes

Custom themes in `themes/`:

- Color schemes and GTK configurations
- Lockscreen themes in `hyprlock/`

## Configuration Structure

```
hypr/
├── hyprland.conf          # Main Hyprland configuration
├── hypridle.conf          # Idle management
├── hyprlock.conf          # Lockscreen configuration
├── pyprland.toml          # Pyprland plugin configuration
├── animations/            # Animation presets
├── hyprlock/              # Lockscreen themes
├── shaders/               # GLSL shaders
├── themes/                # GTK and color themes
├── workflows/             # Workflow configurations
└── ...
```

## Customization

### Changing Themes

Edit `themes/theme.conf` to modify colors, GTK theme, and icon theme.

### Modifying Keybindings

Edit `keybindings.conf` for custom shortcuts.

### Adding Shaders

Place new `.frag` files in `shaders/` and reference them in `hyprland.conf`.

### Creating Workflows

Add new `.conf` files in `workflows/` with specific settings.

## Troubleshooting

### Common Issues

- **Shaders not working**: Ensure GLSL files are valid and paths are correct
- **Themes not applying**: Check GTK configuration and restart Hyprland
- **Audio controls not working**: Verify PipeWire is running and `wpctl` is available
- **Brightness control**: Ensure `brightnessctl` has proper permissions

### Logs

Check Hyprland logs with:

```bash
hyprctl logs
```

## Contributing

Feel free to submit issues or pull requests for improvements.

## License

This configuration is provided as-is. Use at your own risk.
