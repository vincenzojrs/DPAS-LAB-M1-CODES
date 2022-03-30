###### a cura di Vincenzo Junior Striano
# Data Privacy and Security LABS - MSc in Data Science and Management at LUISS Guido Carli (Rome, Italy), commands needed for Kali on Mac ARM64 (M1 or more)


## KALI INSTALLATION:
* Install [Parallels Desktop 17](https://www.parallels.com/it/) or more (30-day free trial, ~80€ lifetime payment) or any other free virtualization software (not available, march 2022). Download a [Kali ISO ARM64 “Bare Metal”](https://www.kali.org/get-kali/#kali-bare-metal) and [create a new VM from an ISO/Image file](https://kb.parallels.com/en/4729) (**not from Parallels "Internal" Installer, look for "Install from your source" in the previous link**) **OR** 
* [Create a bootable USB drive](https://www.kali.org/docs/usb/live-usb-install-with-mac/) with [Kali ISO ARM64 “Bare Metal”](https://www.kali.org/get-kali/#kali-bare-metal) version, empty USB +32GB needed. Everytime you need to run Kali, [plug the USB, turn on the Mac, keep pressing the power button until you access Recovery Mode](https://support.apple.com/it-it/HT201255). Choose to boot the system by the USB **OR**
* [Dual boot installation using a Kali ISO ARM64 “Bare Metal”](https://www.kali.org/docs/installation/dual-boot-kali-with-mac/) **(PRO)**

###### (about the last two options) Unfortunately there are no Webex Client for Linux ARM64, so you won’t be able to install Webex. Moreover, Online Webex will require codecs which are not available for LinuxARM64: you’ll need to follow the lessons using another device (march 2022). 

**LAB LESSONS WHOSE CODE IS NOT DIFFERENT FROM KALI AMD64, WON'T BE LISTED BELOW. ALWAYS TRY TO RUN THE CODE PROVIDED BY THE PROFESSOR, FIRST. IF IT’S NOT WORKING, FOLLOW THIS GUIDE.**

## LAB: MITM
```bash
$ sudo apt install xterm && sudo apt install mininet && sudo apt update && sudo apt upgrade
# run before running the code provided by the professor,
# no other differences with the code provided
```
## LAB: PASSWORD CRACKING
```bash
$ sudo apt install zip && sudo apt install john && sudo apt update && sudo apt upgrade
$ cd Desktop
$ zip nameforzipfolder.zip nameofthefiletozip -P password 
$ zip2john nameforzipfolder.zip > hash.txt
$ john hash.txt
```
## LAB: DOS
Same as MITM

###### scientia est potentia
