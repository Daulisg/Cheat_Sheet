#### This Command will show the working directory

    pwd

#### Use This command to reboot the device

    reboot

#### Will power off the radio but Only a cold reboot will Turn back ON

    poweroff

#### This command will show you which modules are running

    lsmod

#### This Command will show you the logs

    logread

#### Network interfaces

    ifconfig

#### Will reset radio to default

    firstboot

#### To show the dongle version

    cd /tmp# cat prs_version.log

#### Will how the settings on the radio

    uci show

#### Shows the [BusyBox](https://busybox.net/) version

    sh

#### This shows the option requested i.e: uci get wireless.radio1_1.ssid

    uci get

#### This command will set the option requested i.e: uci set wireless.radio1_1.ssid=`new-ssid`

    uci set

#### Will apply the changes after using uci set

    uci commit

#### To show the route

    ip route

#### Will show arp table

    arp

#### To run an iperf server with nepim, also run **nepim help** for options

    nepim

#### To run an [iperf3 server](https://en.wikipedia.org/wiki/Iperf)

    iperf3

#### To run an **Iperf3** server on the radio **-s** is specifying the server mode

    iperf3 -s

#### To set the radio as a client when running iperf3

    iperf3 -p <port> -c <ip> -P5 -t11 -O 01 -R

#### To get a file from the internet after **Internet** is up...

    wget

#### This will show the network settings configurations

    uci show network

#### Use this command when you can't get access thru ssh due to `keygen`...

    ssh-keygen -R <IP>

#### To sh FW version

    cat /etc/version

#### Run this command to restart network

    /etc/init.d/network restart

#### This command will factory reset and reboot

    jffs2reset -y && reboot

#### Will Show the username -If root user is removed, then system wont reboot

    cat /etc/passwd | grep "bin/ash"| cut -d ":" -f 0

#### passwd root, remember to uci set

    Note: To Change the Root password.

#### This Will Show the Username and password and admin rights

    cat /etc/config/users

#### To show the serial number

    cat /etc/qaee.json | grep serial_no

#### To stop the http server [lightTPD](https://www.lighttpd.net/)

    /etc/init.d/lighttpd stop

#### To start the http server

    /etc/init.d/lighttpd start

#### To restart the http server -Will show command not found but will restart...

    /etc/init.d/lighttpd restart

#### Watching rssi thru CLI -For Local and Remote

    watch cat /var/run/stats/wireless.json | grep Rssi

    Note: Watching rssi thru CLI -For Local

    watch cat /var/run/stats/wireless.json | grep LocalRssi

    Note: Watching Data-Rates, the -n flag will grep Rate or Rssi every -n seconds

    watch -n 1 cat /var/run/stats/wireless.json | grep Rate
