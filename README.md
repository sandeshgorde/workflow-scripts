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

### warp-toggle

Turns Cloudflare WARP on or off with one command and shows a desktop notification. Meant to be bound to a key combo.

**Requires:** `cloudflare-warp` (provides `warp-cli`) and `libnotify-bin` (provides `notify-send`).

**One-time setup** (after installing cloudflare-warp):

    warp-cli registration new
    warp-cli mode warp+doh

The toggle only runs connect/disconnect, so the mode you set here stays saved.

**Usage:**

    chmod +x warp-toggle
    ./warp-toggle

Verify it works with WARP on:

    curl https://www.cloudflare.com/cdn-cgi/trace | grep warp

You should see `warp=on`.

## Binding a script to a key combo

Settings, then Keyboard, then Custom Shortcuts, then add a shortcut. Set the command to the full path of the script (for example `/home/youruser/workflow-scripts/warp-toggle`) and press your combo. Use the full path, because `~` often does not expand there.

## License

Use these however you like.
