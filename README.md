# Nokia-8000-4G

Modifications on my nokia 8000 4G run KaiOS

* USB Debug must enabled -> press `*#*#33284#*#*` on dial up on phone
* Use firehose client version 3.52 from https://github.com/bkerler/edl
* Git clone https://github.com/bkerler/edl and run it on Ubuntu
* Install requipment librarys
* Run `adb devices` from cmd for check connection work
* On ubuntu open cmd and run: `edl r recovery recovery.img` for drump a backup stock recovery on computer
* Second stage run: `edl w recovery path-to-recovery-patched.img`
* Run: `edl reset` for reset phone
* Waiting phone reboot
* run `adb reboot recovery` for reboot phone to recovery mode
* from cmd run `adb push` and `adb pull` for check work
