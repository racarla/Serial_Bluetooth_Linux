# Tutorial - Use a bluetooth device like serial in Linux using CLI

This tutorial consist on the installation and configuration of bluetooth in Linux.

## Preface

Bluetooth is still very important in the world today given that a wide range of devices rely on its protocol to perform several operations. Most laptops come with built-in Bluetooth adapters, but even if yours is not, external Bluetooth pens are cheap and plentiful.

Having Bluetooth properly configured on your machine allows you to use a Bluetooth mouse, keyboard, headset or any Bluetooth accessories you may own.

But usually once you have installed some packages and made some adjustments, everything works perfectly, at least that has been my experience.

So if you have had problems connecting to your Bluetooth accessories from your Linux PC, this entry should help you.

## Installing packages

First, you must install the required packages on your computer. If you are in Ubuntu or in a distribution based on Ubuntu, execute the following command:

```
sudo apt-get install bluetooth bluez bluez-tools rfkill
```

## Checking, preparing and starting

Next, make sure that your Bluetooth device is not blocked and also serves to check if the device is connected. You can check with the rfkill utility:

```
sudo rfkill list
```

![alt text](https://raw.githubusercontent.com/racarla/Serial_Bluetooth_Linux/master/bluetooth-linux-rfkill.png)

As you can see in the screenshot above, my Bluetooth device is not blocked. If yours is locked for some reason, you can unlock it using the same rfkill command.

```
sudo rfkill unblock bluetooth
```

Finally, make sure that the Bluetooth service is active by executing the following command.

```
sudo service bluetooth start
```
Note: You can check the bluetooth status service
```
sudo service bluetooth status
```
![alt text](https://raw.githubusercontent.com/racarla/Serial_Bluetooth_Linux/master/bluetooth-linux-service-status.png)

## Search for Bluetooth devices



## Pairing and connection to devices

## Applications

* Connect and communicate with the common serial HC-06 or similar for Arduino and the computer.

## Abbreviations

* CLI - Command Line Interface (Terminal)

## References
* [Setup Bluetooth in Linux](https://maslinux.es/como-configurar-bluetooth-en-gnulinux/) (29/05/2019)
Interesting if you want to make the connection with a graphic tool and also connect a bluetooth headset.
* http://www.linux-magazine.com/Issues/2017/197/Command-Line-bluetoothctl
* https://docs.ubuntu.com/core/en/stacks/bluetooth/bluez/docs/reference/available-commands
* https://blog.dbrgn.ch/2017/8/22/hc06-bluetooth-terminal-on-linux/
* https://gist.github.com/0/c73e2557d875446b9603
* http://manpages.ubuntu.com/manpages/cosmic/man1/rfcomm.1.html

