# OneMix3Pro-OpenCore
Install macOS on your 10th gen OneMix 3 minibooks.

## Compatibility

- **OneMix 3 Pro Koi/ Platinum/ Black with i7 10510Y**: The main model this configuration was developed with and for.
- **OneMix 3 Pro Black with i5 10210Y**: Compatible in theory. Not tested.
- **OneMix 3s Black/ Platinum with i3 10110Y** Compatible in theory. Not tested.
 
## Post-installation tweaks
A few required or otherwise useful steps to take on a running macOS system on your OneMix:

**Changing the display orientation**

To correct the display orientation within macOS, press and hold down `cmd+opt` (`Windows+alt`) and open `System Preferences`. Keep holding down those two buttons and click on `Displays`. The screen orientation option will now appear even for the built-in display. Set it to `90 degrees` for the correct orientation. Alternatively...just download the [Display Rotation Menu](https://www.magesw.com/displayrotation/) app and set the view to portrait flipped

**Disabling Power-related Settings**

In order to achieve a stable sleep, you're responsible of disabling the following:
- Power Nap (if available)
- Wake for Internet Access
- tcpkeepalive (hint: `sudo pmset -a tcpkeepalive 0`)

**Switching `cmd` and `opt`**

In keyboard settings, select the modifier keys option, and switch `cmd` (win) with `opt` (alt)

## What works

- Full hardware acceleration, faked UHD617 Amber Lake-Y
- Audio
- Battery reading and charging recognition
- USB-A port as-well as the USB-C port
- CPU Temperature and voltage/wattage reading
- Internal Wi-Fi via OpenIntelWireless (Big Sur Support)
- Bluetooth via OpenIntelWireless
- Sleep

## What's untested

- Hibernation
- HDMI output

## What's not yet working

- Microphone
- Touchscreen
- Lid Device (Auto triggered after boot; after wake no longer working)
- Bluetooth (After a reboot IntelFirmware stucks at an infinite loop; will no longer boot until a hard shutdown)

## What will never* work

- Intel SD Card Reader
- Bosch Accelerometer
- Focaltech Fingerprint

_* Not unless someone decides to make custom kexts for these, of course._
