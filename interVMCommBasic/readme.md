VM-1: VONE    
VM-2: VTWO  

# Description
The xopera command will be executed in Local VM.   
Upon execution, *readRmtCnt* application will be deployed atop *VONE* vm. The deployed application will read the content of multiple remote files present in *VTWO* vm.


VONE 
=====
IP: 192.168.1.185  
*createFile.sh* script is running in VONE.  
path of *createFile.sh* : *$HOME/*  

Job of this script:  
    create a folder *db*  
    change the current directory to *db*  
    create 100 files with random integer values as content of those files.  
    file names follow the sequence *file1*, *file2*, ... *file100*  
    10sec delay between each file creation  


VTWO
=====
IP: 192.168.1.141   
run *readfile.sh* in *$HOME* directory  
Job of this script:  
    read the content of the remote files from *VONE* vm   
    append those remote contents to *fileCnt.txt* file in *$HOME/rmtFileCnt/*  


Service.yml 
------------  
This is present in local system, where the xopera commmand will be issues.  
this will connect to the *VTWO* vm.  
Deploy the "readRmtCnt" application *$HOME* directory  

"readRmtCnt" application
-----------
 create a shell script file *readfile.sh* in $HOME directory  
 Run the shell script file  

# Assumption
Certain number of files are already created in remote vm *VTWO*  

