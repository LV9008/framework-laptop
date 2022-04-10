# framework-laptop

## Enable Deep Sleep
The framework laptop does not save power in sleep when s2idle is used.
You can turn on deep sleep to save more power at the cost of longer got to and wake from sleep times.

Add the following to /etc/default/grub and reboot
```bash
GRUB_CMDLINE_LINUX="mem_sleep_default=deep"
```
To check:
```bash
cat /sys/power/mem_sleep
```
The output should be:
```bash
s2idle [deep]
```
