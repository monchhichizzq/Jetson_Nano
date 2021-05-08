### Jetson_Nano
### Camera setup 
 
#### 1. Test the camera on Jetson Nano
    
       git clone git@github.com:JetsonHacksNano/CSI-Camera.git
       
      
1. test the gstream (sensor_id: the port of camera on Jetson) 
      
      
     gst-launch-1.0 nvarguscamerasrc sensor_id=0 ! nvoverlaysink

        
     gst-launch-1.0 nvarguscamerasrc sensor_id=0 ! \
     'video/x-raw(memory:NVMM),width=3280, height=2464, framerate=21/1, format=NV12' ! \
     nvvidconv flip-method=0 ! 'video/x-raw,width=960, height=720' ! \
     nvvidconv ! nvegltransform ! nveglglessink -e
     
     
     
     GST_ARGUS: Available Sensor modes :
     GST_ARGUS: 3264 x 2464 FR = 21.000000 fps Duration = 47619048 ; Analog Gain range min 1.000000, max 10.625000; Exposure Range min 13000, max 683709000;
    
     GST_ARGUS: 3264 x 1848 FR = 28.000001 fps Duration = 35714284 ; Analog Gain range min 1.000000, max 10.625000; Exposure Range min 13000, max 683709000;
    
     GST_ARGUS: 1920 x 1080 FR = 29.999999 fps Duration = 33333334 ; Analog Gain range min 1.000000, max 10.625000; Exposure Range min 13000, max 683709000;
    
     GST_ARGUS: 1640 x 1232 FR = 29.999999 fps Duration = 33333334 ; Analog Gain range min 1.000000, max 10.625000; Exposure Range min 13000, max 683709000;
    
     GST_ARGUS: 1280 x 720 FR = 59.999999 fps Duration = 16666667 ; Analog Gain range min 1.000000, max 10.625000; Exposure Range min 13000, max 683709000;
    
     GST_ARGUS: 1280 x 720 FR = 120.000005 fps Duration = 8333333 ; Analog Gain range min 1.000000, max 10.625000; Exposure Range min 13000, max 683709000;
     
     

2. run face detection application

    
    python3 face_detect.py
    

3. ssh test camera on MAC

    
    ssh -X -Y name@ip
    
    export DISPLAY='local ip:0.0'
    

4. repeat the steps 1, 2