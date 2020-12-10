# mac-vpnc
MacOS DNS fix for open connect

Copy to /etc/vpnc, make chmod +x for every script in /etc/vpnc, replace "Wi-Fi" in use-vpn-dns & use-default-dns with interface you using to connect VPN.
You can find interface name by typing in terminal:
```bash
networksetup -listnetworkserviceorder
```
output should be like:
```
(1) Ethernet
(Hardware Port: Ethernet, Device: en0)

(2) Wi-Fi
(Hardware Port: Wi-Fi, Device: en1)

(3) iPhone USB
(Hardware Port: iPhone USB, Device: en5)

(4) Bluetooth PAN
(Hardware Port: Bluetooth PAN, Device: en4)

(5) Thunderbolt Bridge
(Hardware Port: Thunderbolt Bridge, Device: bridge0)
```
If you need VPN DNS on several interfaces - just copy & paste configuration line for each of them.

Fresh vpnc-script can be obtained from https://gitlab.com/openconnect/vpnc-scripts/-/blob/master/vpnc-script
