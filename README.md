# Primer79 ZMK firmware

ZMK shield support for the Yushakobo Primer79 using a nice!nano. The base
layer matches the vendor QMK default layout. The left encoder controls volume,
the right encoder controls display brightness, and pressing the encoders sends
F11 and F12 respectively.

## Bluetooth and output controls

Hold the key in the original right-Win position to access the Fn layer:

- Fn+F1 through Fn+F5 select Bluetooth profiles 1 through 5.
- Fn+Esc clears the currently selected Bluetooth profile.
- Fn+F6 forces keyboard output over Bluetooth.
- Fn+F7 forces keyboard output over USB.

For a clean re-pair, remove the keyboard from the host's saved Bluetooth
devices, select the desired profile, press Fn+Esc, then pair again.

## Hardware safety

The nice!nano is designed to charge a single-cell 3.7 V rechargeable lithium
battery. Do not connect the Primer79's original CR1632 coin-cell battery setup
to a nice!nano, especially while USB is connected. Test the keyboard from USB
power first, and use a correctly wired, polarity-checked 3.7 V rechargeable
battery for wireless operation.

## Building and flashing

GitHub Actions builds both `nice_nano_v2` and legacy `nice_nano` artifacts.
Use the artifact matching the controller revision. Enter the nice!nano
bootloader by quickly pressing reset twice, then copy the corresponding UF2 to
the `NICENANO` drive.
