# Epigrass Vagrant Box

This project creates a Virtual Machine (VM) on your computer running [Epigrass](http://pythonhosted.org/epigrass/index.html).

### Features

- The user interface is displayed in the X Window client of your choice on the host computer (i.e. your laptop)
- Data is synced between your host computer and the Epigrass VM.

### Limitations

- MySQL is **not** installed. You need to use either CSV or sqlite3 database

## Installation Instructions

### MacOS

1. Install [VirtualBox](https://www.virtualbox.org)
2. Install [Vagrant](https://www.vagrantup.com/downloads.html)
3. Install [XQuartz](https://www.xquartz.org)
4. Download or checkout this project.
5. Open Terminal, and change directories to the location of this project.
6. In terminal, execute `vagrant up`. This will take 20 minutes or so, depending on the internets.
7. In terminal, execute `vagrant ssh -C epigrass`. A window will appear displaying the Epigrass user interface.


## Operating Instructions

You can launch epigrass by performing steps 5 - 7 of the installation instructions

When epigrass launches, a new folder will be created in this project's directory called `epigrass-data`. Any files you place in this folder will be visible to the application.

Even when you close the Epigrass window, the VM is still running on your computer. In the project directory, run `vagrant suspend` to shutdown the VM.
