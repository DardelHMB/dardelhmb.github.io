# Fixing a lite brick on a Wii U

## Info
This guide will direct you to repair your lite bricked Wii U.

## What "Lite bricked" means:
Lite bricked is my own term for a Wii U that is bricked due to damaged/missing titles (mainly the Wii U Menu) on the MLC. This can happen while attempting a region change or modifying the system files with FTP.

### IMPORTANT NOTE
This guide requires that your System Settings and System Updater apps are intact and usable. It cannot fix hardware failure (such as a dead Hynix MLC.) For that, I recommend you check out [Lazr's guide](https://lazr1026.github.io/unbrick/#/) on doing a full unbrick if this does not work for you.
Preferably, you should have a full MLC included backup made while the console was still working. This can be used to restore the System Settings and System Updater apps if needed.
If you don't have one, you should make one **right now** (this will need access to the Payloadloader/HBL so if you don't have such access you'll have to do without.

### Disclaimer:
I am not responsible if you further damage your Wii U following this guide. Be sure to follow all instructions EXACTLY and to read CAREFULLY. By using this guide you agree that I am NOT responsible for any further damages done to your Wii U with this guide.
If you have any concerns regarding the legitimacy or accuracy of this guide, please DM me or ping me on the NH server on Discord (@dardelsploon) I'd be more than happy to fix anything wrong/incorrect.

## Getting started:
This guide depends on your current coldboot title.

If you're currently autobooting into the payloadloader (tiramisu/aroma) you can get started [here.](insert next section) FYI, you *will* need access to Tiramisu and the HBL, Aroma will not work if your Wii U menu is damaged.

If you're currently booting into the Wii U menu (no changes) you will need access to either a Raspberry Pi Pico/Zero or a RCM vulnerable Nintendo Switch.
Continue from [here](insert Wii U coldboot section)

If you are using Coldboot Haxchi (CBHC) you *should* be able to use the same guide for users using the Payloadloader. But I make no promises. As soon as you've unbricked your Wii U you should remove CBHC and install the Payloadloader *as soon as possible.*
If you have a CBHC bricked Wii U, go [here](insert CBHC unbrick guide)
