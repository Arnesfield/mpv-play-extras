# mpv-play-extras

Additional mpv scripts for improving some controls.

## Install

You can clone this repository under your `scripts` directory (e.g., `~/.config/mpv/scripts`).

```sh
git clone git@github.com:Arnesfield/mpv-play-extras.git play-extras
```

## Scripts

List of available scripts this package provides.

### [autoplay](lib/autoplay.lua)

Automatically unpauses the video when a file is loaded (plays from the beginning if the video has ended).

This is enabled by default (currently cannot be disabled unless you modify [`main.lua`](main.lua) and remove it).

### [toggle](lib/toggle.lua)

Serves as a slight improvement for toggling between play and pause (`cycle pause`).

This script exposes a script message `play-extras/toggle` which does the same `cycle pause` but will also play from the beginning if the video has ended.

In your `input.conf`, you can override the default behavior (`space`) like so:

```conf
space script-message play-extras/toggle
```

## License

Licensed under the [MIT License](LICENSE).
