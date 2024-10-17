
![](https://github.com/Rick-EV/SolarkCloud/blob/main/logo.png)

## How it works
SolarkCloud Companion will fetch solar system data online, initially posted to the cloud via your Sol-Ark dongle. It does not have any physical interfaces that are connected directly to your inverter. 
Please also note that this add-on only populates sensor values with data. It does not come with any cards to display information.

See full documentation here
https://github.com/Rick-EV/SolarkCloud/blob/main/DOCS.md

## Getting Started

This add-on needs to publish sensor values to Home Assistant's entities via the HA local API in order to function. Therefore, a long-lived access token is required.

### Setting up a long-lived access token.
Click your profile picture at the bottom left of your Home Assistant user interface. Scroll to the bottom and create a long-lived token. The token name is not important for the Solarcloud add-on but, the token key is. Copy the token key and keep it for use later during configuration.

![](https://github.com/Rick-EV/SolarkCloud/blob/main/longlivetoken.png)

### Add this repository to your Home Assistant add-on store
From the "Settings" menu item in Home Asstant's UI go to "Add-ons". In the bottom right-hand corner click "ADD-ON STORE". In the right-hand top corner click the three dots and select "Repositories".
Paste the following repository link and click add then close https://github.com/Rick-EV/SolarkCloud

![](https://github.com/Rick-EV/SolarkCloud/blob/main/addrepo.png)

Refresh the browser page. Right at the bottom you should now see the "SolarCloud" add-on. Simply click on it then click "Install"

![](https://github.com/Rick-EV/SolarkCloud/blob/main/solarsynkaddon.png)


### Provide your SolarCloud.com credentials
After installing this add-on make sure you enter all the required information on the configuration page. Note: if your intentions are to update a Home Assistant installation with a different IP than the one where this addon is installed, you need to generate the long live token on the Home Assistant instance where entities will be updated. 
DO NOT USE localhost or 127.0.0.1 in the IP field, either use the actual IP or hostname. If you implemented an SSL certificate, it is mandatory to use the hostname assigned to the certificate and not the IP. 

![](https://github.com/Rick-EV/SolarkCloud/blob/main/configuration.png)

In case you are unsure what your Sol-ark inverter's serial number is. Log into the solarcloud.com portal and copy the serial number from the "Inverter" menu item.
For multiple inverters separate the inverter serial numbers with a semicolon; Example 123456;7890123

![](https://github.com/Rick-EV/SolarkCloud/blob/main/sunserial.png)

Make sure you also populate the "HA_LongLiveToken" field with the long-lived token that you created earlier on.

### Start the script
After entering all of the required information you can go ahead and start the service script.

![](https://github.com/Rick-EV/SolarkCloud/blob/main/solarsynkstarted.png)

Once started make sure all is working by clicking on the "log" tab. Scroll through the log and check that the sensor data was populated correctly.
Few values will be "0" if you for instance only have a single string of solar panels MPPT-2 values will be "0". If something goes wrong ALL of the sensors will have a "0" or "Null" value. 


