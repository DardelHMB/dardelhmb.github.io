# Information about severe Wii U errors

## Info

This page contains infomation about some errors on the Wii U which you never want to see. Hopefully yours will never end up here.

## Error Code: 160-0103

Starting off strong here, error code 160-0103 indicates a **corrupt MLC.**
The most common cause is a faulty Hynix MLC chip.

**There is no software fix. Do not let YouTube fool you. UDPIH cannot fix this error.**

The only method to fix this is by soldering an sd card to replace the MLC chip. I do not have a guide on this. (But if I find a good one I will place it here)

## Error Code: 160-0105

Error code 160-0105 indicates that your external USB is corrupt.

This can happen for a number of reasons. Most common cause is using a flash drive as external storage, which cause all sorts of funky issues.

In any case, that drive is not likely to be recognised by the Wii U anymore.

If it is a HDD: Extract games/saves via DumpsterU if nessasary (hopefully it can grab them), then format with the Wii U in data management.

If it is a flash drive: **Stop using a flash drive. Grab saves/games from it with DumpsterU if you can, then get a HDD.**

## Error Code: 160-0101

This error code is usually caused when the Wii U cannot boot the Wii U menu. In other words, a **CBHC brick.**
Lucky for you, this is extremely easy to fix now!

Before starting the below guide please note this error is also quite generic, it can occur for a variety of reasons, however UDPIH is still useful to dump your logs to find out what's happening in this case.

What you need:
- A Raspberry Pi Pico/Zero OR a hackable Nintendo Switch
- A USB C-A cable if using a Switch
- Patience (you'll see why)

Note: I recommend a Pi Pico over the zero, that way, you can use it for [de_fuse](https://lazr1026.github.io/unbrick/#/) if needed later.

If you're using a Pi Pico/Zero, follow the instructions on the [Github repo](https://github.com/GaryOderNichts/udpih#instructions) for booting recovery_menu, I will only provide instructions for the UDPIH nxpayload.

1. Download [updih_nxpayload](https://github.com/GaryOderNichts/udpih_nxpayload/releases/latest)
2. Also download [recovery_menu](https://github.com/GaryOderNichts/recovery_menu/releases/latest) and place it on the root of your Wii U's SD card
3. Either place it in `/bootloader/payloads` on your sd card and boot it with Hekate `Payloads --> udpih_nxpayload.bin`, or inject it with your favourite payload injector
4. Connect your Switch to the Wii U with a USB C-A cable. Do not turn on the Wii U or activate the UDPIH gadget yet.
5. Power on your Wii U
6. Wait for the Wii U logo to appear on your TV/Gamepad then activate the UDPIH gadget
Note: You need to do this **as soon as you see the Wii U logo.** Too early and you won't get display out. Too late and your console will hang on the boot screen or boot normally. This will take a few tries (or you get lucky). If you fuck it up, power off your Wii U and try again.
7. Once you're in the recovery_menu, open `Set Coldboot Title` and change it back to the Wii U menu.
8. Navigate to `Shutdown`, and now your Wii U should be fixed!

Extra: If you need to fix a bad theme, but forgot to use autoboot, use [my recovery_menu-mod](https://github.com/DardelHMB/recovery_menu-mod/releases/download/1.2/recovery_menu) to set the coldboot title to Health and Safety and restore your backup theme from the HBL. **Now you can stop installing themes. Use SDCafiine if you want to use themes or this WILL happen again.**

## Blinking blue light

I'm sorry for your loss.

A blinking blue light indicates **IOSU is not booting.**

The cause is SLC corruption. Fixing it will require hardmod. I do not have a guide on how to replace the SLC or repair it.

If you were happening to use isfshax (de_fuse too I think?), or otherwise see the minute menu, this is normal. No action is required.


## That's all for now
Thanks to the NH Kurisu error repository for some extra info on some of these errors.

Most of this is based on my own experience (a lot of which is seeing people in NH have some of these issues).

If you have any improvements, feel free to open a PR or issue on the Github.

Page created by DardelHMB. See the source [here](https://github.com/DardelHMB/wiiuerrorinfo)
