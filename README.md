# IoT-project
<h1>IoT-setup and configuration</h1>

 ### [For packet tracer](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Project consist of a simple setup of an IoT environment in a manufacturing industry. The goal of this project was to enable employee to have remote access to the manufacturing operation. With Packet Tracer I have set up wireless access point and connected  the server plus IoT devices. The Water drain IoT devices is responsible for draining water out of the tank. The Trip Sensor and the Siren works together to inform employee of any failure in the production system. Temperature monitor and Thermostat are used to monitor and adjust temperature for the production system.
<br />


<h2> Utilities Used</h2>

- <b>Packet Tracer</b> 
  

<h2>Environments Used </h2>

- <b>Windows 11</b> (pro)

<h2>Program walk-through:</h2>

<p align="center">
Step1 choose a wireless equipment, for this project we are going to be using HomeRouter-PT-AC wireless Router. navigate to the bottom left of packet tracer and first click on Network Device, second Wireless Devices, third select the HomeRouter. Just left click on it and left click on the main console. <br/>
<img src="https://imgur.com/Xf5nh2Z.png" height="80%" width="80%" alt="Adding wireless access point"/>
<br />
<br />
Step 2: import a server:  <br/>
 <br />
Navigate to the bottom left and click on End Devices, left click on server as well. 
Come back to the main console there will be a plus sign instead of the pointer cursor. 
Click the anywhere on the console to paste the server.
 <br/>
<img src="https://i.imgur.com/Caoi1v5.png" height="80%" width="80%" alt="Adding a remote server"/>
<br />
<br />
Step 3: add the IoT devices. <br/>
 <br />Navigate to the far-left bottom of the console and select End Device, at bottom of that select industrial and navigate to device section. We are going to add four IoT devices. 
Click on Temperature monitor and drag it up to the main console. 
Repeat this process for all the other three devices (Thermostat, Trip Sensor, Water Drain)
 <br/>
<img src="https://i.imgur.com/OEqtLiq.png" height="80%" width="80%" alt="Adding IoT devices"/>
<br />
<br />
Step 4 is to connect all the devices to the access point:  <br/>
 <br />we are going to start with the server first.
Connect the server with a Copper straight-Through cable to the access point.
navigate to far left again and select connection and click on copper straight-through.
Left click on server and select FastEthernet0 then left click on the wireless router and choose any interface of your choice. Here I choose G/E1 
<br/>
 
<img src="https://i.imgur.com/DYjDDAm.png" height="80%" width="80%" alt="Connecting all devices to the access point"/>
<br />
<br /> Step 4a: Configure the connection between the Wireless access point and the server.
  <br/>
  <br />left click on the server, navigate to config tap and enable the dhcp.
Confirm the DHCP is working by checking the ip address of the server in the FastEthernet 

  <br/>
    <br />
  <br/>
<img src="https://i.imgur.com/WFXXs31.png" height="80%" width="80%" alt="Configuration DHCP Between server and access point wireless"/>
<br />go to the Services tap of the server and select IoT then turn on.
<br />
<br />
<img src="https://i.imgur.com/HeVh5if.png" height="80%" width="80%" alt="Turning on the IoT service"/>
<br />Now let go to the Desktop tap to enter our credentials. Click on desktop then IoT monitor.
<img src="https://i.imgur.com/GIJBo1x.png"  height="80%" width="80%" alt="Signing up for the remoter registration"/>
</p>
<br />NOTE: it will not let you sign in as we have not created a log in credentials yet. So we are going to create one in the next step. Click on sign up now.  enter any username of your choice here I’m going to use admin as the username and   passw0rd as the password. click enter. 
<br />
<img src="https://i.imgur.com/tVLdxcO.png" height="80%" width="80%" alt="Registration Server Login"
<br />
  <br/>
  <br />There should not be any devices on the IoT Monitor yet. IT should look like this when you login.
<br />
<img src= "https://i.imgur.com/GtognPd.png" height="80%" width="80%" alt="Registration Server Menu"
<br/>Step 4b:Now let configure the wireless access point to connect the IoT devices.
<br/>
<br/>There is not much we are going to change from the default settings. We are only going to change the security settings to wpaw2 personal. 
Click on the Wi-Fi and navigate to the GUI tap. click on the wireless tap and change the default SSID to linker.  Click on wireless Security tap. Enable 2.4GHz Security Mode by selecting WPA2 Personal.
Set a passphrase. In my case it is going to be linker123. Feel free to use it or create your own.

<br/>
<img src= "https://i.imgur.com/GouMKib.png" height "80%" width"80%" alt="Wireless access point Gui"
<br/>NOTE:  you will not see the save bottom until you scroll down to the bottom. 
Click on save and exit the menu.

<br/>
<br/>Now we are going to connect IoT device to the Wi-Fi. 
The first one is Trip Sensor. The trip sensor does not have a wireless interface as of now. We need to add a wireless interface for us to connect to it wirelessly.
Click on the trip sensor when the menu come up, click on advance and navigate to the I/O config tap.
From network adapter choose PT-IOT_NM_1W.
Next click on config tap and enter the SSID of the WI_FI (linker). choose WPA2-psk and enter the pass phrase which is linker123 close the window for the connection to happened.
For the temperature monitor, left click on it. Click on wireless0 and select WPA2-PSK. 
enter the SSID of the WI-FI (linker
enter the Pass phrase.  linker123
<br/>
<img src= "https://i.imgur.com/79ON3WJ.png" height "80%" width "80%" alt= "Connecting Trip sensor to wirless access point"
<br/>then close the tap to establish connection.<br/>
<br/>
<br/>

Repeat the above procedure for the other two devices.<br/>
<br/>Now let connect it to the registration server. <br/>
<br/>Click on trip sensor and the details configuration will show up. Go to config tap, <br/>
<br/>Select Remote server.<br/>
<br/>Enter the Ip address of the server. In my case the
 Ip address: 192.168.0.10<br/>
<br/>Username: admin2<br/>
<br/>Password: passw0rd

<br/>
<img src= "https://i.imgur.com/wk6D2Qm.png" height "80%" width "80%" alt="connecting Trip Sensor to the rigistration server"
<br/>If Connection changes to refresh, then your connection was successful. Close the whole Trip Sensor configuration.
<br/>
<br/>Check to confirm if the device has been added to the remote registration server. 
<br/>
<br/>Click remote server and navigate to Desktop tap.
<br/>
<br/>Select IoT monitor. Enter your credentials. 
<br/>
<br/>You should be able to see Trip Sensor in the IoT monitor from the remote registration server.
<br/>
<br/>Add Water Drain IoT to remote registration server. <br/>
 <br/> Click on the Water Drain device and navigate to the to the config tap. <br/>
 <br/>Select remote server and the enter the ip address, username and password<br/>
 <br/>Ip address: 192.168.0.10<br/>
 <br/>Username: admin2<br/>

 <br/>password: passw0rd<br/>
 <br/>check if the connection was successful in IoT monitoring interface.<br/>
 <img src= "https://i.imgur.com/kFtVBaD.png" height "80%" width "80%" alt="Water drain added to the Registration server"
 <br/>Repeat the same step for other devices you want to add.
 <br/>
  <br/>Managing the devices from the server GUI. <br/>
  <br/>You can manage all the devices in this interface. We are going to set conditions for one or two devices in here.<br/>
  <br/>Click on conditions and click add.<br/>

   <img src= "https://i.imgur.com/CaVd8K6.png" height "80%" width "80%" alt="Setting condition for the devices." 

   <br/>Click the drop-down arrow in +condition and Select Trip Sensor, leave it to on and true.<br/>
   <br/><br/>
   <br/>Then click the other drop-down arrow in +Action and select Siren from the list of devices<br/>
   <br/>Also make it on and true. Press ok.<br/>
   <br/>
   
   <br/>
   <br/>Now if you test it by holding alt on your keyboard and passing the mouse on the trip sensor the siren will turn red but will not turn off once you click away from the trip sensor. So, we need to make it do so.<br/>
   <br/>Click on condition again and click add in the next menu to set the condition.<br/>
   <br/>Follow the picture below. Make sure to press ok.<br/>
   <img src= "https://i.imgur.com/CC6lzQd.png" height "80%" width "80%" alt="Setting condition for Trip Sensor and Siren"
   

  
  







<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
