# GPSinBDMAP
GPS recevie data including latitude and longitude, and then publish the data to baidu map web, and display location dynamic in 1s.

hardware:UM220-III/3-N/北斗GPS芯片/时钟授时/232输出/千寻位置MH16-L1   
taobao link:https://item.taobao.com/item.htm?spm=a1z09.2.0.0.34e02e8d3x5iFJ&id=39425855477&_u=11sqvu1ja1a2  
![GPS product](https://github.com/Zippen-Huang/GPSinBDMAP/blob/master/gps.jpg)

software:ubuntu and ROS

package Usage method:
step1: download the software package into ros workspace

step2: apply a baidu map develeper account, and then modify roslibjs/example/BDMAP_v1_2_28.html, replace appid and key.

step3: run some cmdline as follows
```cpp
$ roslaunch nmea_navsat_driver gpsStart.launch //start gps
```
```cpp
$ roslaunch nmea_navsat_driver rosrecord.launch //if you want to record gps data, then start the nodes
```
```cpp
$ roslaunch rosbridge_server rosbridge_websocket.launch  //launch brideg between ros and web
```
step4: run BDMAP_v1_2_28.html  

![effect display](https://github.com/Zippen-Huang/GPSinBDMAP/blob/master/gps.png)  
