<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/klor-font-logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/klor-font-logo-bright.svg">
  <img alt="KLOR logo font" src="/docs/images/klor-font-logo-bright.svg">
</picture>

# ZMK CONFIG FOR THE KLOR SPLIT KEYBOARD

[Here](https://github.com/GEIGEIGEIST/qmk-config-klor) you can find the QMK config for the KLOR.\
[Here](https://github.com/GEIGEIGEIST/klor) you can find the hardware files and build guide.

KLOR is a 36-42 key column-staggered split keyboard. It supports a per key RGB matrix, encoders, OLED displays, a Pixart Paw3204 trackball and four different layouts, through brake off parts.

![KLOR layouts](/docs/images/klor-layouts.svg)

Polydactyl is the default layout. If you choose one of the other layouts you can use the matching template in the default keymap.

## KNOWN ISSUES

- The encoder on the secondary side doesn't work yet. This is a limitation of ZMK.
- Need to add the code for the Pixart Paw3204 trackball.
- Need to add Seed XIAO controller support

### Steps

## Fork or Clone Repository
   - Click **Fork** in the top right to copy this repo to your GitHub account, or
   - Run `git clone` locally.

   > Forking is recommended, because GitHub Actions will automatically build your firmware.

## Keymap Editing
   -  use the [ZMK Keymap Editor](https://nickcoutsos.github.io/keymap-editor/):
   - Map your repository to the editor to see the current settings
   - Make changes on the site and save
   - your repository will be compiling the build with your new configuration
   - read below on flashing your keyboard

## Dongle Flashing
   - Turn all devices off
   - go to **Actions → your latest run → Artifacts** and download the firmware (`.uf2`) files.
   - Flash the dongle with the **appropriate** `settings_reset` file.
   - Flash the dongle controller with the `dongle` file.
   - Flash the first half with the the `settings_reset` file.
   - Flash the first half with the `left` or `right` files.
   - Repeat last two steps for the other half.

> [!WARNING]  
> When using both Nice!Nano and Seeed XIAO microcontrollers, make sure you are flashing them with the correct files!

