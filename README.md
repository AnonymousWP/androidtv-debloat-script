# About

* ADB Shell script to uninstall all bloated apps that comes with some Android TV's, that cannot be uninstalled using the TV UI with the remote

## Download ADB

* Make sure you have ADB on your machine first: [See here](<https://www.xda-developers.com/install-adb-windows-macos-linux/>)

## How to run

* Clone this repo
* If you want to check which apps are installed on your Android TV, then first you need to connect to your Android TV using the command below to

```bash
adb connect <your tv local ip here>:5555
```

* Then, you need to list out all your Android TV installed apps via the command below

```bash
adb shell cmd package list packages "|cut -f 2 -d": >> path/to/your/desktop/packages.txt
```

* Copy all the app names that you want to uninstall, line by line into a `bloat.txt` file in the **SAME** directory with `uninstall-bloat.sh` script
* Or if you already have the list of what apps you want to uninstall, add them in the `bloat.txt` line by line and do the steps below
* Make sure you have `enabled USB debugging` located in your `Developer` settings on your Android TV
* Run this script using the command below

```bash
sh uninstall-bloat.sh
```

* Follow the script instructions.
* Enjoy
👌
