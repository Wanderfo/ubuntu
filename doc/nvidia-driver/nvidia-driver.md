# Install nvidia driver for gtx1070

## Download driver
Download the driver from nvida website [http://www.geforce.cn/drivers] chose `GeForce GTX 1070` `Linux 64-bit` then search or [raw_link](http://cn.download.nvidia.com/XFree86/Linux-x86_64/367.44/NVIDIA-Linux-x86_64-367.44.run)

## Install driver 
To install the driver you need to close Xwindow first.Press `ctl+alt+F1` then insert the user name and password
```
$ sudo /etc/init.d/lightdm stop
$ chmod u+x NVIDIA-Linux-x86_64-367.44.run
$ sudo ./NVIDIA-Linux-x86_64-367.44.run
```
Then accept the license and others chose the default
> NOTE: If you use HDMI, there maybe no signal on your monitor

Reboot and you will find the dirver had been ready like this
![driver ready](dirver-ready.png)
