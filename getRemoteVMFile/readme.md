# Description
Fetch a file from remote VM (OpenStack VM) and store in local filesystem

## Parameters (Remote VM)
IP of remote VM: 192.168.1.1  
Remote filename: id_rsa.pub  
path to remote file: /home/centos/.ssh/id_rsa.pub  

## Local VM
Location to keep the fetched file: /tmp/opera2/

## Command to run
cd path/to/service.yml
opera deploy test service.yml

## Assumption  
The VM is already created and in running state  
