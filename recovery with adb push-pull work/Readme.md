* USB Debug must enabled -> press `*#*#33284#*#*` on dial up on phone
* Use firehose client version 3.52 from https://github.com/bkerler/edl
* I'm run it on Ubuntu
* Open cmd and run install requipment librarys and clone firehose client from from https://github.com/bkerler/edl
   ```
    sudo apt install adb fastboot python3-dev python3-pip liblzma-dev git
    sudo apt purge modemmanager
    sudo systemctl stop ModemManager
    sudo systemctl disable ModemManager
    sudo apt purge ModemManager
    
    git clone https://github.com/bkerler/edl.git
    cd edl
    git submodule update --init --recursive
    sudo cp Drivers/51-edl.rules /etc/udev/rules.d
    sudo cp Drivers/50-android.rules /etc/udev/rules.d
    python setup.py build
    sudo python setup.py install
   ```
* Connect phone to computer and run `adb devices` from cmd for check connection work
* On ubuntu open cmd and run: `edl r recovery recovery.img` from folder edl for drump a backup stock recovery on computer
* Run: `edl w recovery path-to-recovery-patched.img` -> to write patched image to recovery partition on phone
* Run: `edl reset` to reset phone
* Waiting phone reboot
* Run `adb reboot recovery` to reboot phone to recovery mode
* From cmd run `adb push` and `adb pull` to check it work
