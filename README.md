# workflow-scripts

Small scripts I use to speed up my Linux workflow. Built on Pop!_OS with GNOME on X11.

## Scripts

### oled-mode / oled-reset

Tweaks screen contrast and gamma for a darker, easier-on-the-eyes display.

- `oled-mode`: clears any existing profile, sets contrast to 97 and gamma to 0.92
- `oled-reset`: puts everything back to normal (gamma 1.0)

**Requires:** X11 only. These do not work on Wayland.

    sudo apt install xcalib x11-xserver-utils

**Usage:**

    chmod +x oled-mode oled-reset
    ./oled-mode
    ./oled-reset

To trigger them with a key combo, go to Settings, then Keyboard, then Custom Shortcuts, add a shortcut, and set the command to the full path of the script (for example `/home/youruser/workflow-scripts/oled-mode`).

## License

Use these however you like.
