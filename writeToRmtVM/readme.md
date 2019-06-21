# Description

Write information to remote file system.  
Precisely, this would add the public key ( either of the local system or of any other system) to the *authorized_keys* of remote VM  
This would help for further secure remote connect.  

# Remote VM
IP: 192.168.1.5  
This would modify $HOME/.ssh/authorized_keys file  

# local VM
Location of public key: /tmp/opera/id_rsa.pub  
The content of the */tmp/opera/id_rsa.pub* would be appended to the end of *$HOME/.ssh/authorized_keys* present in remote VM  

## Command to run
cd path/to/service.yml
opera deploy test service.yml

## Assumption
The VM is already created and in running state  
