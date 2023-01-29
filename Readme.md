# Vagrant virual machine with python3.11

Your need install vagrant and virtualbox for up this configuration.

Your need install [vagrant](https://github.com/hashicorp/vagrant-installers/releases/tag/v2.3.4.dev%2Bmain "vagrant") and  [virtualbox](https://www.virtualbox.org/ "virtualbox") for up this configuration. Optional you can use [make](https://www.gnu.org/software/make/ "make").

### Step 1

Download box jhcook/osx-elcapitan-10.11 for virtualbox from [vagrantup](https://app.vagrantup.com/senglin/boxes/win-10-enterprise-vs2015community "vagrantup").

### Step 2

Clonr this repository: 

``git clone https://github.com/codesshaman/vagrant_windows_10``

### Step 3

Copy/move box and named it "macos". In the terminal go inside the project folder:

``cp ~/Downloads/downloaded_file path_to/vagrant_windows_10/windows``

``cd vagrant_windows_10``

### Step 5

Inicialize configuration:

``vagrant box add senglin/win-10-enterprise-vs2015community windows``

or with make:

``make build``

### Step 6

Install configuration:

``vagrant up --provider=virtualbox``

or with make:

``make``

### Step 7

reboot virtual machine and login with login and password "vagrant".

### Step 8

Connect to VM from terminal:

``ssh vagrant@192.168.58.93``

or with make:

``make connect``

## Howto use this configuration?

1. Open external folder "<myproject>" or "<myproject>/src" in Pycharm
2. Use VM for project creation and external project folder for use git

Change PATH: ``export VAGRANT_HOME=".vagrantboxes"`` or ``make path``

Start: ``vagrant up`` or ``make``

Stop: ``vagrant halt`` or ``make down``

Restart: ``vagrant reload`` or ``make re``

Hybernation: ``vagrant suspend``

Delete VM: ``vagrant destroy`` or ``make clean``
