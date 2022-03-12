# Connecting Whirlpool
This section will demonstrate how to connect the Whirlpool desktop client to your Tanto full node and your Samourai Wallet. With this configuration, you will be able to have your UTXOs mixing non-stop in the backround from your desktop client and powered by your own full node. When you mix from mobile only, the mixing stops as soon as you shut down your mobile Whirlpool client in Samourai Wallet. 

First, you will need to download the Whirlpool client appropriate for your operating system. The different options along with accompanying developer signatures can be found [here](https://samouraiwallet.com/download) and detailed installation instructions can be found [here](https://docs.samourai.io/whirlpool/desktop). Be aware you will likely need to install Open JDK as well which is covered in the installation instructions. 

<p align="center">
 <img src="assets/RoninUI14.png">
</p>

Once you have your Whilpool client installed and your Samourai Wallet connected to your RoninDojo Tanto, you can make an SSH connection to the RoninDojo and start the Whirlpool service. The Whirlpool .onion URL you need is not available through the RoninDojo UI dashboard. The SSH connection can be made with the same username password you used for the RoninDojo UI.

Once connected, navigate to `Samourai Toolkit` > `Whirlpool`:

<p align="center">
 <img width="450" src="assets/RoninUI15.png">
 <img width="450" src="assets/RoninUI16.png">
</p>

Then select `start`, a script will run briefly and then you can hit any key to return to the main menu when prompted. 

<p align="center">
 <img width="450" src="assets/RoninUI17.png">
 <img width="450" src="assets/RoninUI18.png">
</p>

With the Whirlpool service started, and back at the main menu, now navigate to `Credentials` > `Whirlpool`

<p align="center">
 <img width="450" src="assets/RoninUI19.png">
 <img width="450" src="assets/RoninUI20.png">
</p>

This is where you can retrieve the .onion URL you need to use in the Whirlpool client Graphical User Interface (GUI) to get it configured. Highlight this URL and use `ctrl+shift+c` to copy it to your clipboard. 

<p align="center">
 <img src="assets/RoninUI21.png">
</p>

Now open the Whirlpool client application you installed earlier. Select the `Advanced: remote CLI` option and where it says `https://my-cli-host:8899` paste the .onion URL from your RoninDojo terminal. Depending on whether or not your are running a Tor daemon or just the Tor browser, you may need to select either `9050` or `9150` for appending the Tor proxy. Leave the API key blank, this will automatically be handled once initialized. Then click on `Connect`. 
 
<p align="center">
 <img src="assets/RoninUI22.png">
</p> 

Give the GUI some time, Tor connections can take a little while. You may need to try this a couple times before the connection is made. But once the connection is made, you will be presented with a screen asking you to input the Whirlpool pairing payload from your Samourai Wallet. In Samourai Wallet, click on the 3-dot menu in the upper right-hand corner and select `Settings` > `Transactions` > `Pair to Whirlpool GUI` at the bottom. This will display a QR code that contains your Whirlpool payload. Simply click on the QR code option in the desktop GUI and this should launch your webcam then hold up the QR code on your mobile so the camera can scan it. 

<p align="center">
 <img src="assets/RoninUI23.png">
</p> 

Once received, then click on `Initialize GUI`.

<p align="center">
 <img src="assets/RoninUI24.png">
</p> 

Next, enter the passphrase for your Samourai Wallet and click on `Sign in`.

<p align="center">
 <img src="assets/RoninUI25.png">
</p> 

Once signed in, you should be able to see your balances, mixing activity, and then you can set targets for how many mixes you wish to achieve. You can even generate deposit addresses from the Whirlpool GUI.

<p align="center">
 <img src="assets/RoninUI26.png">
</p> 
