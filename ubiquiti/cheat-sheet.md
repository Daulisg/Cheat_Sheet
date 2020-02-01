#### To Get the Model number

    cd /etc
    cat board.inc | grep board_nam

#### Will show the encryption and type

    cd /var/tmp
    cat system.cfg | grep aaa.1.wpa

#### SSID of the radio

    cd /var/tmp
    cat system.cfg | grep wireless.1.ssid

#### IP of the radio

    cd /var/tmp
    cat system.cfg | grep netconf.6.ip

#### If auto-nego is on/off

    cd /var/tmp
    ethtool eth0.21 | grep Auto

#### IP of all clients (used -p to parse)

    cd /var/tmp
    wstalist -p | grep lastip

#### All running config

    cd /var/tmp
    cat running config   ////Confirmar

#### Mac Address of the device

    cd /sys/devices/virtual/net/br1
    cat address

#### EIRP Limit Status

    cd /var/tmp
    cat system.cfg | grep radio.1.obey

#### The Channels set on the input fields

    cd /var/tmp
    cat running.cfg | grep radio.1.scan_list.channels

#### The Channels set on the input fields

    cd /var/tmp
    cat running.cfg | grep radio.1.scan_list.channels
