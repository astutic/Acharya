# Acharya
A Data Centric MLOps tool for your Named Entity Recognition projects.

# Download
Download the acharya binary latest release for your system. Our current release is at https://github.com/astutic/Acharya/releases/tag/v0.1.0-alpha

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
