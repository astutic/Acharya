# Acharya
A Data Centric MLOps tool for your Named Entity Recognition projects.

# Download
Download the acharya binary latest release for your system. Our current release is at https://github.com/astutic/Acharya/releases/tag/v0.1.0-alpha

* [Intel Mac binary](https://github.com/astutic/Acharya/releases/download/v0.1.0-alpha/acharya.0.1.0-alpha.darwin.amd64.bin) | SHA256: 97d3011105bba18cd1d7a0975c190ae593abf3bab877d254a646863df2151cce 
* [M1 Mac binary](https://github.com/astutic/Acharya/releases/download/v0.1.0-alpha/acharya.0.1.0-alpha.darwin.arm64.bin) | SHA256: 60856871965edf6651bb7b233222fc4e00c53ee29c28b804b16587a0a852e369
* [Linux binary](https://github.com/astutic/Acharya/releases/download/v0.1.0-alpha/acharya.0.1.0-alpha.linux.amd64) | SHA256: 379609ff81eb94a7291401707368a6505ac15c34d19859f48663b490df75b051
* [Windows binary](https://github.com/astutic/Acharya/releases/download/v0.1.0-alpha/acharya.0.1.0-alpha.windows.amd64.exe) | SHA256: 642a82a2ecb5cfbad6e195b69ae3d359c1be3cc2707eb62094b91e7a5029abb1


# Initial Run and Setup
Installation and Setup for Acharya is not required, Acharya detects it running for the first time and runs the initial setup when run for the first time.
To start Acharya type the following command in a terminal/command prompt 
It is recommended to create a separate folder to run acharya. Acharya will create a data folder and a temp folder to store its data.

On *sh shells
```bash
#copy the downloaded file to the newly created acharya folder and run the following commands.
chmod +x acharya
./acharya
```

On Powershell and COMMAND in Windows 
```powershell
acharya.exe
```

Acharya will generate a password for the default user admin@localhost

The UI will be accessible at http://localhost:3000

Login to the UI with admin@localhost as the username and the password displayed on the terminal/command prompt screen.

It is recommended that the users change this password from the UI

# Using Acharya
Login to the Acharya UI using a web-browser and access the URL seen in the output of the above command. The default URL would be https://localhost:3000

# Commandline Tasks
Acharya also supports multiple command line tasks like uploading data to a project or initiate a training (which could be scheduled via cron or Windows task scheduler)
Please read the documentation available here.
