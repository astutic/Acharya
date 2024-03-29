![Acharya logo](/docs/images/logo/acharyaLogox100.png "Acharya Logo")
# Acharya
A data-centric annotation tool to increase the accuracy of your Named Entity Recognition projects which helps

- Rapidly identify and fix labelling errors in your dataset. 
- Import/export datasets in multiple formats, train a model and use it to aid in annotation process. 
- Setup an MLOps pipeline to experiment with different algorithms on the same data and increase their accuracy and performance in a data-centric way.

# Download
![Downloads](https://img.shields.io/github/downloads/astutic/acharya/total)

Download the community edition acharya binary latest release for your system. Our current release is at https://github.com/astutic/Acharya/releases/tag/v0.3.4-alpha

* [Intel Mac binary](https://github.com/astutic/Acharya/releases/download/v0.3.4-alpha/acharya.0.3.4-alpha.darwin.amd64.bin) | SHA256:  0109da5b30c98417856386b08384b3cce1501a6cdc9a3e8f1bc3849ad1faf2f4
* [M1/M2 Mac binary](https://github.com/astutic/Acharya/releases/download/v0.3.4-alpha/acharya.0.3.4-alpha.darwin.arm64.bin) | SHA256: 4f5cdbd7c341c11de4b9bc49d18d4b516a719e0d14d7b5d1ca94f458a93ea89b
* [Linux binary](https://github.com/astutic/Acharya/releases/download/v0.3.4-alpha/acharya.0.3.4-alpha.linux.amd64) | SHA256: 036e7ed0e9215c46e09085f5bb10e14c1b04ff5c593e513cf5030ab50d8a45b2
* [Windows binary](https://github.com/astutic/Acharya/releases/download/v0.3.4-alpha/acharya.0.3.4-alpha.windows.amd64.exe) | SHA256: adbf9d4ba8aaa9a7ae0f331604d1b90060392d47d8a171d8808e10c05d6cd5c0


# Initial Run and Setup
Installation and Setup for Acharya are not required, Acharya runs the initial setup when run for the first time.
To start Acharya type the following command in a terminal/command prompt 
It is recommended to create a separate folder to run acharya. Acharya will create a data folder and a temp folder in the folder where it is run to store its data.

On *sh shells
```bash
# copy the downloaded file to the newly created acharya folder and run the following command. Change the binary as per your platform
chmod +x acharya.0.3.4-alpha.darwin.amd64.bin
./acharya.0.3.4-alpha.darwin.amd64.bin
```

On Powershell or COMMAND in Windows 
```powershell
acharya.0.3.4-alpha.windows.amd64.exe
```

Windows firewall will show a prompt where it will ask whether it should allow acharya to listen to port 3000. Please allow it.

The UI will be accessible at http://localhost:3000

The UI will prompt the user to set a password for the default user admin@localhost

# Using Acharya
Login to the Acharya UI using a web-browser and access the URL seen in the output of the above command. The default URL would be http://localhost:3000

For more use case driven docs, Check the [How-to's](#how-to's) section.

### 5 minute demo

https://user-images.githubusercontent.com/61645553/137438387-690a9d86-cebc-408e-abe5-0e52258b76bd.mp4

## Getting Started
Acharya Docs are available at https://acharya.astutic.com/docs/get-started/acharya-installation

## How to's 
1. [Change admin password](#change-admin-password)
2. [Create a new Project](#create-project)
3. [Upload data to project](#upload-data)
4. [Annotate data in workbench](#workbench)
5. [Gain insights from dashboard and modify data](#dashboard-reports)
6. [Add Algorithms](#add-algorithms)
7. Train algorithms with the data
8. Insights from training and data modification

## Change admin password
Login to acharya UI and navigate to Settings menu shown on the sidebar. Once on the settings page, click on the Admin password tab, and change your password.

## Create project
Login to acharya UI, the default page would be the Projects page. If you are on any other page, access the Project page via the sidebar. Click on the Create project button or the Add project button and Choose a name for the project and description and click on Create button.

## Upload data
To upload data to a Project, from the Projects landing page, click on the project ID, which would open the project. From the sidebar choose Upload to open the Upload data page.
Based on the format of your data, choose the Data format accordingly. There is also an option to upload plain .txt data, or if the text data is not as a file, you can paste the text data on the editor and upload it. While uploading the data, the user can select the data to be marked for training or test/evaluation or keep it pending (not used for training or test/evaluation.). The user can change this parameter later from workbench screen.

## Workbench
Data uploaded via upload or command-line tasks are stored as records in Acharya. These records can be viewed and modified on the workbench screen.
The data shown on the workbench screen can be annotated by selecting the data and choosing an appropriate entity.

[Read more about Workbench features](https://acharya.astutic.com/docs/tutorial-basics/using-workbench)

## Dashboard Reports
Acharya project dashboard focuses on data-centric reports about the data in the project. 
[See more about the dashboard section](https://acharya.astutic.com/docs/tutorial-basics/data-centric-reports) 

### Check entity data bias from entity distribution
Entity distribution shows how many annotations belongs to each entity. If the number of annotations of a particular entity is less or more as compared to other entities, it shows that the dataset is biased against or towards that entity. This report gives an insight that what kind of new data should be sourced into the project to balance the entity distribution.

### Classifications
Classifications list the words classified against each entity. This table helps in identifying words which are classified as what entities. If a word is classified as more than one entity then it is important to verify such annotations and confirm the validity of that annotation.

This table also helps to know the occurrences of each annotated words in the dataset. 

### Missed Classifications
Missed classifications show the words that have been classified once in the dataset and missed at other locations of the dataset. This is very important to identify mistakes where the annotator might have either missed classifying the word or might have wrongly classified that word.

Sorting on Missed Records would let the user know annotations which might have been missed by the annotator

And sorting on Classification Counts would let the user know annotations that might have been wrongly annotated by the annotator.

### Anomalies
Anomalies highlight those annotations where the system feels the annotation might be a mistake.
This might need annotation correction of the underlying data to be modified.

### Unclassified words
This table helps in identifying unclassified words in the project. Instead of browsing the dataset, this table helps sort the words based on their word length and number of occurrences.

### Algorithms trained
Shows a quick glance of how well each algorithm has been trained on the dataset, and which one is the best trained algorithm.

## Add algorithms
Please read the [Algorithms section](https://acharya.astutic.com/docs/get-started/add-algo-to-project) for detailed information.

To add algorithms to the project, the user needs to specify the algorithm details via a yaml configuration.

The current release of acharya only support running of algorithms via a docker container, so all the algorithms added into acharya would require either a docker image or a Dockerfile

# Command-line Tasks
Acharya also supports multiple command line tasks like uploading data to a project or initiate a training (which could be scheduled via cron or Windows task scheduler)

The command-line tasks can be listed via the following command which needs to be run in a terminal/powershell/command prompt
```powershell
.\acharya.0.3.4-alpha.windows.amd64.exe tasks list
```

the output would be

```
Available grifts
================
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe compare        # Compare Results of 2 Train
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe convert        # To convert input data to another format.
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe copyFile       # copyFile [src] [dst project:algo:dstDirpath] Copies file to running algorithm container/VM
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe entities       # To list, add and modify entities in a NER Project.
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe export         # Export data in a Project in required data formats.
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe import         # To import external data into a project.
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe login          #
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe logout         #
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe project        # To add and delete projects
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe requireAuth    #
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe train          # Train Algorithm
C:\acharya\acharya.0.3.4-alpha.windows.amd64.exe users          # User related operations
```

certain tasks would require login and the task would prompt for the same.

# Advanced settings
## Running on a different port
To run acharya on a different port, set the environment variable PORT to the appropriate port number by prefixing PORT=port_number before the command
