#### Show cpes history on ports

    show sysl lo v r | grep CPE

#### To look at the Gam history

    Show syslog local volatile reverse

#### To show the status of a port

    show cpe port-status

#### To show the clock

    show clock

#### Will show the Signal-to-noise ratio/interference on the specified gam port

    show ghn snr interface ghn2 | grep ghn2.cpe

#### Will show the Signal-to-noise ratio/interference on the range of ports specified \*/

    show ghn snr interface range ghn1-ghn10

#### Will show the Signal-to-noise ratio/interference on remote devices

    show ghn snr remote

#### Will show the Signal-to-noise ratio/interference on remote specified

    the two on the left or the two on the right
    ghn14.cpe 247 212 - 93 79
    show ghn snr remote | grep ghn11.cpe

#### Will show noise on port 2 of the gam

    show ghn noise interface ghn2

#### Will show noise on all ghn remotes

    show ghn noise interface ghn2

#### Will show the wire length in meters for a specific port

    sh ghn wire-length interface ghn2

#### Will show line rate that this customer can have

    show ghn line-rate remote | grep ghn14.cpe

#### Will show the interface descriptions

    sh int | inc In|De

#### Show the Mac on a port

    show mac port ghn2

#### To check Gam temp

    show environment

#### To reboot the remote port on the gam or the link (But will work only if it sees it)\*/

    ghn reboot interface ghn4 remote

#### To reboot the local port on the gam

    ghn reboot interface ghn4 remote

#### To reboot port ghn23

    ghn reboot int ghn23

#### To show the port informatio like the speeds for ghn2 in this example, remember

    that when grepping,ghn2, will show 2 and also 22,23,24 because it has the 2
    ghn2 - UP UP - 247M/ 241M 93M/ 90M 1 1 -

    	show port information | grep ghn2

#### To show if the Modem/link is upgraded (should say; 0 Ready: initial status)

    show ghn fw-upgrade

#### To show the configuration on a specific port/locally

    i.e. of a xe1:
    Interface name : xe1
    Switchport mode : trunk
    Ingress filter : enable
    Acceptable frame types : vlan-tagged only
    Default Vlan : 1
    Configured Vlans : 1 10 21
    i.e. of a ghn:
    Interface name : ghn1
    Switchport mode : access
    Ingress filter : enable
    Acceptable frame types : all
    Default Vlan : 10
    Configured Vlans : 10 4094

    	show interface switchport bridge 1

#### To show all vlans used for this gam on specific ports

    show vlan all

#### Will show the user session

    show users | grep \*

#### Will show the sync-port if master and if connected or not

    show sync-port

#### Will show the ip set for the Gam

    sh ip int | grep vlan21

#### Will show the Fiber port status (If Fiber and not copper i.e. xe1/xe2)

    end the info from the sfp:
    Interface Name : xe1
    Transceiver status : Equipped, link up
    Type of transceiver : SFP or SFP+
    Code of transceiver : 1000BASE-LX
    Cable Length : 10 Km [ Single Mode ]
    Speed of transceiver: 1250 Mbps
    Laser wavelength : 1310 nm
    Connector type : LC
    Vendor name : Zaram
    Vendor part number : LTI-SFP-LX
    Vendor rev. level :
    Vendor serial number: SU161703130702
    Manufacturing date : 170320
    DDM Calibration : Internal
    DDM Temperature : 39.76 'C (Warn : L -40.00 H 85.00)
    (Alarm: L -45.00 H 90.00)
    DDM Vcc(supply vol.): 3.26 V (Warn : L 2.80 H 3.70)
    (Alarm: L 2.70 H 3.80)
    DDM TX bias : 24.51 mA (Warn : L 0.10 H 90.00)
    (Alarm: L 0.00 H 100.00)
    DDM TX power : -6.36 dBm (Warn : L -9.00 H -3.00)
    (Alarm: L -10.00 H -2.00)
    DDM RX power : -8.85 dBm (Warn : L -23.01 H -1.00)
    (Alarm: L -23.98 H 0.00)
    DDM power state : TX ON RX ON

    	show port transceiver

#### Will show the counter on the port specified

    If this is good::: xe1 10666573 3682927 155519 106 0
    If this is shut/no traffic ::: xe2 0 0 0 0 0
    Check if the switch or gam have the port shut and check light levels with: show port transceiver

#### Check if the port is shut/down with : show port information | grep xe2

    show port statistics counter | grep xe2

#### Will show the mac on port ghn1

    show mac port ghn2

#### Will show all the ghn pairing remote or links will skeep the ports without a link

    show ghn pairing remote

#### Will show all the ghn pairing local or ports but wont skeep, will show NO when down\*/

    show ghn pairing local

#### Will show the rate limiting on the interface/port \*/

    show ghn rate-limit interface ghn2

#### Will show the rate limiting on the interface/port but for .cpe (Just a grep of the above)

    show ghn rate-limit interface ghn2 | grep ghn2.cpe

#### Will show the rate limiting on the interface/port but for .cpe (Just a grep of the above)

    show ghn rate-limit interface ghn2 | grep ghn2.cpe
