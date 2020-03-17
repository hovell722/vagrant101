# Vagrant and Virtual Box 101

This repo setup a simple ubuntu machine.

## What is Vagrant?

Allows us to manage and provision Virtual Machines.

It also allows us to pull images of VM from its marketplace.



## What is Virtual Box?

Is the SW that does the heavy lifting of creating said machines.


## Find out basic Vagrant commands

how to start a vagrant file?
```
vagrant init <box_distribution_image>
```

how to start a VM?
```
vagrant up
```

how to destroy a VM that is running?
```
 exit
vagrant destroy
```

how to shut down a VM without destroying it?
```
exit
vagrant reload
```

## Create a ubuntu 18.04 server
Using Vagrant,
```bash
> vagrant init
# edit the file
# change the config.vm.box to the box you want
```

## How to update the list of packages

`sudo apt-get update -y`

## What does -y do?

Gives confirmation before you get the prompt

## How to install packages

`sudo apt-get install (package) -y`

## How to set up an internal IP

in the vagrantfile write:

`config.vm.network "private_network", ip: '(chosen ip)'`

Then paste the `(chosen ip)` into a browser and it should show a welcome page

## How to run packages

`sudo systemctl start (package)`

## How to check if package is running

to show all running processes:
- `ps aux | grep (package)`
