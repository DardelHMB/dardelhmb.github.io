# Looking for problems from the latest log

There are a few signs to lookout for when reading through the latest log. I will show a few.

## Serious problems

These are some more serious problems, which will likely require de_fuse to fix if you cannot boot normally.

`### MEDIA ERROR ###, dev:xxxxx` can mean different things depending on whats in `dev:`

`dev:odd01`: The disc drive, this can be ignored.

`dev:mlc01`: The MLC, this is more concerning and what you do not want to see.

(Taken from V10lator's [nand-aid guide](https://gbatemp.net/threads/using-nand-aid-to-repair-a-broken-emmc-fix-160-0103-system-memory-error.636361/)) A `MEDIA ERROR` on mlc01 means that the eMMC itself noticed it can no longer retrieve the data error free. **This indicates a failure in the MLC.**

This would need nand-aid in order to fix it. You can follow [V10lator's guide](https://gbatemp.net/threads/using-nand-aid-to-repair-a-broken-emmc-fix-160-0103-system-memory-error.636361/) for this.


`DATA CORRUPTION` is less serious. It indicates a file is corrupt in the MLC. It's important to look through the logs for specifics, as otherwise `DATA CORRUPTION` could mean anything.



Thanks to V10lator and their (and its respective contributors)[nand-aid guide](https://gbatemp.net/threads/using-nand-aid-to-repair-a-broken-emmc-fix-160-0103-system-memory-error.636361/) for most of the detailed info

