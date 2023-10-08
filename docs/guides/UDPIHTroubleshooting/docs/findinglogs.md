# Determining the latest log

recovery_menu does not output the logs in order. We need to read a binary file to find the latest.

Along with the logs, you should also have `meta.bin`. Open this file with a hex editor.

[image](https://github.com/DardelHMB/udpih-troubleshooting-guide/blob/main/docs/image/image.png)

You should see something like this. We need to convert the hex number to decimal and then mod by 100

In this case, the hex number is `036B`, so in a modulo calculator, input `b=` as 0.36 and `a=` as 100. You should now see the output (in this case 0.28). The latest log is 28.


Thanks to Lazr for telling me how to do this, I would not have figured this out on my own lmao


Continue to [Looking for problems from the latest log](/docs/problemfinding.md)
