# Item Catalog Project

# Project Overview
Item Catalog web application that uses the full stack development skills.  Project would cover Python code to perform backend CRUD operations with the ProgreSQL database and using Google Authentication for user login.  Front end coding involves understanding the use of Bootstrap stylesheet and user web interface.

## Packages required
* sqlalchemy
* ProgreSQL
* google_auto_oauthlib

### Google API Client Key Instruction
1. Sign in at `https://console.developers.google.com/apis/`
2. Create a new Web application
3. Go to Credential under `APIs & Services`
4. Add the following to the field `Authorized JavaScript origins`
```
http://localhost:8000
```
5. Add the following the field `Authorized redirect URIs`
```
http://localhost:8000/login
http://localhost:8000/catalog
http://localhost:8000/oauth2callback
```

## Quickstart
* Step 1:  [Installing the Virtual Machine Instruction ](https://classroom.udacity.com/nanodegrees/nd004/parts/51200cee-6bb3-4b55-b469-7d4dd9ad7765/modules/c57b57d4-29a8-4c5f-9bb8-5d53df3e48f4/lessons/5475ecd6-cfdb-4418-85a2-f2583074c08d/concepts/14c72fe3-e3fe-4959-9c4b-467cf5b7c3a0?contentVersion=5.0.0&contentLocale=en-us) tools called Vagrant and VirtualBox to manage the VM needed to run this project python code against the database for log analysis.
* Step 2:  [Install VirtualBox](https://www.virtualbox.org/wiki/Download_Old_Builds_5_1).  VirtualBox is the software that actually runs the virtual machine.  Install the platform package for your operatuing system.  Vagrant will use VirtualBox to launch VM.
* Step 3:  [Install Vagrant](https://www.vagrantup.com/downloads.html).  Vagrant is the software that configures the VM and lets you share files between host computer and VM filesystem via folder '/vagrant/'
* Step 4:  [Download the VM configuration for Vagrant](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/April/5acfbfa3_fsnd-virtual-machine/fsnd-virtual-machine.zip).  This will contain the directory `vagrant` which contains the `VagrantFile`.
  Alternatively, it is possible to use Github to fork or clone the repository
  [https://github.com/udacity/fullstatck-nanodegree-vm](https://github.com/udacity/fullstatck-nanodegree-vm)
* Step 5:  Start the Virtual Machine, change directory using `cd` into the `/vagrant` directory and use the command ```vagrant up```, then log into it with ```vagrant ssh```
* Step 6:  In order to use the Google Authentication API, run command:
```
sudo pip install google_auth_oauthlib
```

* Step 7:  In the Vagrant ssh enter the following:
Create the database using ProgreSQL
```
psql -c "CREATE DATABASE catalogdb"
```

* Step 8:  Setup the database tables for the operations with command below:
```
python init_database.py
```

* Step 9:  Run the project by running 'app.py'
```
python app.py
```

## JSON endpoint for API request
- Possible API are the followings:
```
http://localhost:8000/catalog/JSON
http://localhost:8000/catalog/categories/JSON
http://localhost:8000/catalog/PUT_CATEGORY_NAME_HERE/items/JSON
http://localhost:8000/catalog/PUT_CATEGORY_NAME_HERE/PUT_ITEM_NAME/JSON
```

#### Cleaning Up Project
* Run command to drop the table from ProgreSQL
```
psql -c "DROP DATABASE catalogdb"
```
