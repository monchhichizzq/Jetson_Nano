# Jetson_Nano

###  1. Maximum power capacity

The nvpmodel command handles two power options for your Jetson Nano: 

(1) 5W is mode 1 
(2) 10W is mode 0. 

The default is the higher wattage mode, but it is always best to force the mode before running the jetson_clocks command.


    sudo nvpmodel -m 0