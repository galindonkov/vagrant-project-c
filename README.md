### Description

A project that creates three ```vagrant boxes``` using single Vagrant file.

### Installed softwares needed prior to using the project

- VirtualBox software installation : [link for VirtualBox](https://www.virtualbox.org/wiki/Downloads)

- Vagrant software installation : [link for Vagrant](https://www.vagrantup.com/docs/installation/)

### The repo is having following files

- File ```Vagrantfile``` : Has the configuration for vagrant, about what type of VM we want, once set, executing vagrant up will have our clean environment

### How to use the repo

- Clone this repo to your local machines : `git clone git@github.com:galindonkov/vagrant-project-c.git`

- Change to the currently added directory : `cd vagrant-project-c/`

- Execute `vagrant up` to build your local DEV environments

- Once the DEV environments are created, list to check them by : ```vagrant status``` and the result will be :
```
Current machine states:

web01                     running (virtualbox)
web02                     running (virtualbox)
mysql                     running (virtualbox)
```

- Above output is a proove that three virtual machines ```web01, web02 and mysql``` are created successfully and you can connect either to web01 by ```vagrant ssh web01``` to web02 by ```vagrant ssh web02``` or to mysql by ```vagrant ssh mysql```

- In order to test whether the web servers work, connect to web01 or web02 first :
     ```vagrant ssh web01/2```
     - Check assigned ip address by : ```ip -4 a```
     - Open the ip address into the browser and you should see message like below:
     ```
     Welcome to nginx!

     If you see this page, the nginx web server is successfully installed and working. Further configuration is required.
    ```
 - On order to test whether the mysql server works, connect to ```mysql``` first :
     ```vagrant ssh mysql```
     - Once got the command prompt, execute command ```mysql``` to get into mysql command line tool and the following prompt should appeard:
      ```mysql>``` 
 
- Once you finish with the test type `exit` to leave the Vagrant-built virtual machine.

- Bear in mind that the Vm will remain running, so in case it is not needed anymore you can either shut down the running machine Vagrant is managing by `vagrant halt` or using `vagrant destroy` to stop the running machine and destroy all resources that were created during the machine creation process.
