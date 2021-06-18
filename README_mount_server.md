### Jetson_Nano
### 


### Find the culprit sshfs process:
    
    $ pgrep -lf sshfs


### Kill it:

    $ kill -9 <pid_of_sshfs_process>
      
### sudo force unmount the "unavailable" directory:

    $ sudo umount -f <mounted_dir>
       

    
