# Dumping logs

In order to look at the logs, we need to dump them with recovery_menu.

If you don't know how use UDPIH, follow the instructions [here (RCM payload)](https://github.com/GaryOderNichts/udpih_nxpayload#instructions) and [here (pi pico/zero)](https://github.com/GaryOderNichts/udpih#instructions)

## Dumping

After booting into recovery_menu, select, `Dump Syslogs`, or, if you're navigating blindly, press EJECT once, then POWER once. The logs should now be dumped to `logs` on the root of your sd card.


There will be around 100 logs in `logs`. We now need to figure out which one is the latest as they are not in order (and I highly doubt you want to go through ALL 100 logs)

Continue to [Determining the latest log](/docs/findinglogs.md)
