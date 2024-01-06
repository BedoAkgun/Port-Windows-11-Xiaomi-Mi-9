<img align="right" src="https://raw.githubusercontent.com/erdilS/Port-Windows-11-Xiaomi-Pad-5/main/nabu.png" width="425" alt="Windows 11 Running On A Xiaomi Pad 5">


# Running Windows on the Xiaomi Pad 5

## Installation

### Partitioning your device

### Prerequisites
- Brain
- [Recovery Image](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.0/recovery-cepheus.img)

- [UEFI](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/1.0/boot-cepheus.img)

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

### Notes:
> [!Warning]\
> if you delete any partitions via diskpart later on or now windows will send a ufs command that gets misinterpreted which erase all your ufs
> All your data will be erased! Backup now if needed.
> 
> These commands have been tested.
> 
> Ignore `udevadm` warnings
> 
>  Do not run the same command twice
> 
> DO NOT REBOOT YOUR PHONE if you think you made a mistake, ask for help in the [Telegram chat](https://t.me/woacepheus)
>
> 
> Do not run all commands at once, execute them in order!
>
> YOU CAN BREAK YOUR DEVICE WITH THE COMMANDS BELOW IF YOU DO THEM WRONG!


#### Boot recovery through the PC with the command
```cmd
fastboot boot <recovery.img>
```
##### Run the partitioning script

> If it asks you to run it once again, do so

> This is **optional** but you can **set custom sizes using this script**

> To set custom sizes do ```adb shell partition [TARGET WINDOWS SIZE IN GB]```

> Make sure you do not add GB at the end, just the number

```cmd
adb shell partition
```

#### Check if Android still starts
just restart the tablet, and see if Android still works
If isn't boot or looping or animation, use MIUI recovery or other recoveries for wiping data.


### [Next step: Installing Windows](/guide/English/2-install-en.md)
