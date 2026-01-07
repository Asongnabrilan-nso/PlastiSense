Connecting to WInFiDEL ("Log In" Process)
There is no traditional "Log In" screen for the web interface itself. The security is handled by the WiFi connection.

Step 1: Initial Setup (The "Login")
When the device is fresh or reset, it creates its own WiFi network. This is where you "log in" by providing your home WiFi credentials.

Power on your XIAO ESP32-C3 device.
On your phone or computer, look for a WiFi network named SK-WInFiDEL-Setup.
Connect to this network.
A page should pop up automatically ("Captive Portal").
If it doesn't pop up, open a browser and go to http://192.168.4.1
Click Configure WiFi.
Select your home/office WiFi network.
Enter your WiFi Password.
Click Save.
The device will now save these credentials, disconnect from your phone, and connect to your home network.

Step 2: Accessing the Interface
Once the device is connected to your home network, anyone on that network can access it.

Connect your phone/computer back to your Home WiFi.
Open a browser and go to:
http://winfidel.local
Note: If winfidel.local doesn't work (common on some Windows setups or Androids), you will need the device's IP address. You can find this in your router's device list, or by monitoring the Serial output (USB) when the device boots.
Step 3: Using the API
The API is open to anyone on the network. You do not need a username or password.

View Dashboard: http://winfidel.local/index.html
Settings: http://winfidel.local/settings.html
Raw Data (API): http://winfidel.local/api/v0/diameter/read
NOTE

If you messed up the WiFi password in Step 1, you can reset the settings via the Serial Monitor or by reflashing the device, and start over from Step 1.