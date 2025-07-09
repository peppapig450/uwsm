# Universal Wayland Session Manager (UWSM)

UWSM transforms standalone Wayland compositors into robust, system-managed graphical sessions with proper environment handling, XDG autostart support, and clean shutdown sequences.

## Why USM?

- **Robust Session Management -** Leverage systemd's battle-tested process management for your Wayland session, with proper startup/shutdown ordering and dependency handling.

- **Seamless Environment Handling -** Automatic environment variable propagation between login shell, systemd, and applications.

- **Compositer Agnostic -** Works with Sway, Hyprland, Labwc, Wayfire, and any Wayland compositor with minimal configuration.

- **XDG Standards Compliance -** Full support for XDG autostart, desktop entries, and terminal integration out of the box.

## At a glance

```bash
# Install (example for Arch)
pacman -S uwsm

# Select and launch compositor
uwsm select
uwsm start default

# Launch applications properly
uwsm app firefox.desktop
uwsm app -T  # Terminal in app slice

# Integrate with shell profile
if uwsm check may-start && uwsm select; then
    exec uwsm start default
fi
```

## Getting Help

- **Documentation Issues**: Found something unclear? [Report it](https://github.com/Vladimir-csp/uwsm/issues)
- **General Questions**: Check [Troubleshooting](advanced/troubleshooting.md) first
- **Feature Requests**: See [Development](advanced/development.md) for contribution guidelines
