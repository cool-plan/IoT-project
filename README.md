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
<img src="https://i.imgur.com/HeVh5if.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Turning on the IoT service"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
