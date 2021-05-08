### Jetson_Nano
### Virtual Environment for python
 
      
#### 1. install virtualenv
    
    sudo apt-get install virtualenv


#### 2. create venv 

    python3 -m virtualenv -p python3 <chosen_venv_name>
    
    
#### 3. Activate virtual environment

    source <chosen_venv_name>/bin/activate
    
#### 4. Install python wheels
    
    pip3 install <package-name>
    
#### 5. Officially install tensorflow-gpu on Jetson

    https://docs.nvidia.com/deeplearning/frameworks/install-tf-jetson-platform/index.html

#### 6. Test gpu

    import tensorflow as tf
    gpu_device_name = tf.test.gpu_device_name()
    print(gpu_device_name)
    
    from tensorflow.python.client import device_lib
    local_device_protos = device_lib.list_local_devices()

#### 7. Deactivate virtual environment

    deactivate

    
