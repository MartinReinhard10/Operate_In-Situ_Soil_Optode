This Repository includes Python scripts that enables operation of the In-Situ imaging system.
Run the script GUI_Control.py on Raspberry Pi to operate the system through an interface. Some packages require Linux operating system and will NOT run on Windows or Mac OS

For data processing of images please go to: https://github.com/MartinReinhard10/In-Situ_Soil_Optode_Data_Processing

Please refer to the paper ... for further information regarding the in-situ imaging system for planar optodes in soils.
For additional questions please contact: martinreinhard@bio.au.dk

---
**Setup of Raspberry Pi:**

- Download Raspberry Pi Imager v1.7.3 to PC or MAC

- Write Raspberry Pi OS (Debian Bookworm 64-bit) with Desktop to MicroSD card.

- Connect Raspberry Pi to a monitor, boot and create new user.

- Connect to WiFi mobile hotspot in Terminal: ```sudo nano /etc/wpa_supplicant/wpa_supplicant.conf```

    Edit the wpa_supplicant.conf file:
````
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    country=<YOUR TWO LETTER COUNTRY CODE>

    network={
        ssid="<YOUR NETWORK NAME>"
        psk="<YOUR NETWORK PASSWORD>"
        key_mgmt=WPA-PSK
    }
````

- Reboot Raspberry Pi

- Update Raspberry Pi

- Enable VNC and I2C communication in Raspberry Pi Configuration

- Download Visual Studio Code to Raspberry Pi. See guide: https://code.visualstudio.com/docs/setup/raspberry-pi

  -   Install Python and Jupyter Notebook extensions in VS code

- Open VS Code and clone this repsitory via URL: https://github.com/MartinReinhard10/Operate_In-Situ_Soil_Optode

- Create a Virtual Environment in working directory in VS code terminal: ```` python3 -m venv .venv --system-site-packages ````

- Activate Virtual environment in terminal: ```` source .venv/bin/activate ````

- Install requirements.txt to get all dependencies. In terminal: ```` pip install -r requirements.txt ````
