# Tutorial - Use a bluetooth usb or card like serial in Linux

This tutorial consist on the installation and configuration of bluetooth in Linux.

## Preface

Bluetooth is still very important in the world today given that a wide range of devices rely on its protocol to perform several operations. Most laptops come with built-in Bluetooth adapters, but even if yours is not, external Bluetooth pens are cheap and plentiful.

Having Bluetooth properly configured on your machine allows you to use a Bluetooth mouse, keyboard, headset or any Bluetooth accessories you may own.

But usually once you have installed some packages and made some adjustments, everything works perfectly, at least that has been my experience.

So if you have had problems connecting to your Bluetooth accessories from your Linux PC, this entry should help you.

## Installing

First, you must install the required packages on your computer. If you are in Ubuntu or in a distribution based on Ubuntu, execute the following command:

```
sudo apt-get install bluetooth bluez bluez-tools rfkill
```

## Checking

Next, make sure that your Bluetooth device is not blocked and also serves to check if the device is connected. You can check with the rfkill utility:

```
sudo rfkill list
```

Insert the screenshot

As you can see in the screenshot above, my Bluetooth device is not blocked. If yours is locked for some reason, you can unlock it using the same rfkill command.

```
sudo rfkill unblock bluetooth
```

Finally, make sure that the Bluetooth service is active by executing the following command.

```
sudo service bluetooth start
```

## Search for Bluetooth devices

## Emparejamiento y conexión a dispositivos

## References
* [Setup Bluetooth in Linux](https://maslinux.es/como-configurar-bluetooth-en-gnulinux/)
Interesting if you want to make the connection with a graphic tool and also connect a bluetooth headset.
