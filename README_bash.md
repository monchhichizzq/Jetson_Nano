### Jetson_Nano
### Modify bashrc file


### open bashrc
    
    sudo vi ~/.bashrc or gedit ~/.bashrc


### add path 

    export PATH="/usr/local/cuda-10.2/bin:$PATH"
    export LD_LIBRARY_PATH="/usr/local/cuda-10.2/lib:$LD_LIBRARY_PATH"
      
### setup 

    source ~/.bashrc
       

    
