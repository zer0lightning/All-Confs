# Flashing Juniper Switches

**Prerequisites**
- [SuperPutty](https://www.puttygen.com/superputty) or iTerm on MacOS

- TFTP Server if you are flashing a batch of switches.

- USB to Serial Adapter 

**Configure [SuperPutty](https://www.addictivetips.com/windows-tips/superputty-windows-gui-application-that-can-open-putty-ssh-client-in-tabs/) or [iTerm](http://korishev.com/blog/2014/02/28/iterm2-broadcast-input/)**

- Multiple Sessions and tabs

- Set Shortcut to switch tabs easily

<img src="https://raw.githubusercontent.com/zer0lightning/all-confs/master/superputty.png" alt="SuperPutty"
	title="SuperPutty Multiple Tabs" width="550" height="350" />



**Entering JunOS Bootloader**

- [Recovery](https://www.juniper.net/documentation/en_US/junos/topics/task/configuration/authentication-root-password-recovering-qfx-series.html)

**EX4300 Enterprise Switch** 
```
install --format tftp://the.ip.tftp.server/jinstall-ex-4300-packagename-signed.tgz
```

**EX4200 Enterprise Switch** 
```
install --format tftp://the.ip.tftp.server/jinstall-ex-4200-packagename-signed.tgz
```

**Entering CLI**

```
cli
```

**Show Commands**

```
show system snapshot media internal
show system alarms
show chassis alarms
show chassis hardware 
show virtual-chassis
```

**Adding License**

```
request system license add 
show system license
```

**Shutting Down**

```
request system halt at now
```

**Unset Commands**
```
unset gateway
unset netmask
unset ipaddr
unset serverip
```
