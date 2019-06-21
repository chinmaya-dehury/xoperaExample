VM1: VONE
VM2: VTWO

VONE
=====
"createFile.sh" script is running in VONE. 
path of "createFile.sh" : $HOME/

Job of this script:
    create a folder 'db'
    change the current directory to 'db'
    create 100 files with random integer values as content of those files.
    file names follow the sequence 'file1', 'file2', ... 'file100'
    10sec delay between each file creation


VTWO
=====
run 'readfile.sh' in $HOME directory
Job of this script:
    read the content of the remote files from VONE vm 
    append those remote contents to 'fileCnt.txt' file in $HOME/rmtFileCnt/


Service.yml
------------
this will connect to the VTWO vm.
Deploy the "readRmtCnt" application $HOME directory

"readRmtCnt" application
-----------
 create a shell script file 'readfile.sh' in $HOME directory
 run the shell script file

