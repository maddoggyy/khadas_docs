title: How To Connect to Wi-Fi
---

For desktop system you can setup Wi-Fi via GUI easily, so in this tutorial we just talk about how to connect to Wi-Fi under command line. For Ubuntu/Debian server we can use `NetworkManager` to setup Wi-Fi.

### Scan Wi-Fi hotspot
```
khadas@Khadas:~$ nmcli d wifi list
IN-USE  SSID                          MODE   CHAN  RATE        SIGNAL  BARS  SEC
        VIM                           Infra  2     195 Mbit/s  92      ▂▄▆█  WPA
        Wesion                        Infra  7     260 Mbit/s  84      ▂▄▆█  WPA
        VIM_5G                        Infra  161   405 Mbit/s  84      ▂▄▆█  WPA
        HP-HOTSPOT-48-LaserJet M1218  Infra  7     54 Mbit/s   69      ▂▄▆_  WPA
        ChinaNet-xjCH                 Infra  13    270 Mbit/s  67      ▂▄▆_  WPA
        BRGCN_GUEST                   Infra  1     405 Mbit/s  64      ▂▄▆_  WPA
        BRGCN                         Infra  1     405 Mbit/s  62      ▂▄▆_  WPA
```
You will find the Wi-Fi hotspot you can connect to.

### Connect to Wi-Fi hotspot
```
khadas@Khadas:~$ sudo nmcli d wifi connect your_ssid password your_password
[sudo] password for khadas:
Device 'wlan0' successfully activated with '206ab399-3822-4652-ba4c-64847af0bce9'.
```
*Note: Replace the `your_ssid` & `your_password` to your SSID and password.*

### Disconnect Wi-Fi
```
khadas@Khadas:~$ sudo nmcli d disconnect wlan0
Device 'wlan0' successfully disconnected.
```
