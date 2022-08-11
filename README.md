
Based on [Xamarin.Android - Bluetooth Chat](https://docs.microsoft.com/en-us/samples/xamarin/monodroid-samples/bluetoothchat/) example, source code [here](https://github.com/xamarin/monodroid-samples/tree/main/BluetoothChat)

This is an app that shows SpO2 from an old classic bluetooth device BerryMed without a screen.

<img src="https://user-images.githubusercontent.com/13341477/184039213-2e5b2036-b2a8-4f04-b461-85d622ba0d2e.png" width="50%" height="50%">


Protocol can be found here: https://github.com/zh2x/BCI_Protocol or in this [pdf file](BCI%20Protocol%20V1.2.pdf).

Huge thanks to Zhu Xiaoxin who responded to my email and said ~~wrong way!!~~ "The sync bit is the Most Significant Bit, not the Least Significant Bit." Keep it in mind.


This is a quick half an hour project to get SpO2 level only from this device. No fancy interface, no other data.

<img src="https://user-images.githubusercontent.com/13341477/184053397-469ac8f9-9bdb-4334-8182-f8e733ffdff2.png" width="20%" height="20%">


Hints:
1. To check if your device compatible - try the app Serial Bluetooth Terminal [link to google play](https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal) and check if you receive any data in the terminal. If you can't see anything - this app won't work.
This is what you should see:

<img src="https://user-images.githubusercontent.com/13341477/184053642-1d35a59e-59ab-411e-8189-6e77bd2328de.png" width="20%" height="20%">

2. As this is a classic bluetooth - your phone should be paired to the BerryMed. I filtered out bluetooth device list by the names containing 'Berry' only [here, in this line](DeviceListActivity.cs#L101). Remove this line if your device name doesn't have Berry in it. 
3. Do not press 'Send' button.
