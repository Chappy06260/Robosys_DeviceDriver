# Description
Make device driver with Raspberry Pi 3 model B+ <br>
Operate three LEDs using Raspberry Pi with linux. <br>
![mq1](https://user-images.githubusercontent.com/50652151/101313947-dedbd500-389a-11eb-9bba-37b5c9db4200.jpg) <br>
Used lecture materials of Robosys as a reference. <br>
https://github.com/ryuichiueda/robosys2020.git


# Requirements

|No.|Item Name|Quantity|
|:---:|:---:|:---:|
|1|Raspberry Pi 3 model B+|1|
|2|Bread board|1|
|3|LED|3|
|4|Cable|7|
|5|150Ω Resistor|3|

# Circuit diagram
![キャプチャ](https://user-images.githubusercontent.com/50652151/101168661-19692600-367f-11eb-98eb-d5c2cc75d4ee.PNG)

# How to use
**Build**
```python
$ git clone https://github.com/Chappy06260/Robosys_DeviceDriver.git
$ cd Robosys_DeviceDriver
$ make 
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0 
```
**Unbuild**
```python
$ sudo rmmod myled
```

**Run**
```python
$ echo command > /dev/myled0
```

**command list** <br>
```python
0: Turn off all LED 
1: Turn on only LED1 
2: Turn on only LED2 
3: Turn on only LED3 
4: Turn on  all LED 
5: Flash like wave
```

**video** <br>
[Experiment video](https://youtu.be/g7YNr11Z7pQ)
