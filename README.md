# ags-bar
An opinionated bar based on the GNOME status bar that works out of the box.
It is built with [AGS](https://github.com/Aylur/ags) and meant to be used on hyprland with
home-manager.

## Usage
Home-manager is required to use this bar.
Import this flake by adding the following to your inputs:
```nix
inputs.ags-bar = {
  url = "github:andreashgk/ags-bar";
  # Optional, but recommended.
  inputs.nixpkgs.follows = "nixpkgs";
};
```
After importing this flake, add the `ags-bar.homeModules.default` module to your imports and add the
following config to your home:
```nix
services.ags-bar.enable = true;
# Enable this if you want the bar to configure the necessary hyprland settings for you. Without this
# the bar will not automatically start on launch.
services.ags-bar.integrations.hyprland.enable = true;
```
