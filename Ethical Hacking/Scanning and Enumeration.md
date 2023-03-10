
# Airmon-ng

>Airnon-ng is used to see WI-FI networks and what is connected to them

### Start Airmon

Change wireless adaptor to monitor mode
```bash
airmon-ng start interface
```
---
### Run airmon without Arguments

Documentation: [Airodump-ng](https://www.aircrack-ng.org/doku.php?id=airodump-ng)

```bash
airodump-ng interface-mon
```

Example Output:

| BSSID | PWR | RXQ | Beacons |  \#Data, | \#/s | CH | MB | ENC | CIPHER | AUTH | ESSID
|---|---|---|---|---|---|---|---|---|---|---|---|
| 00:09:5B:1C:AA:1D | 11 | 16 | 10 | 0 | 0 | 11 | 54. | OPN |  |   | NETGEAR
| 00:14:6C:7A:41:81 | 34 | 100 | 57 | 14 | 1 | 9 | 11e | WEP | WEP |  | bigbear

---

### Run Airmon with Set Mac Address

This allows you to see devices communicating on a set network

```bash
airodump-ng --bssid mac-address interface-mon
```


# Nmap

>Nmap is used to scan systems to identify open ports, applications or software versions running on a network

**Do <ins style="color:red">Not</ins> have the Adaptor in Monitor Mode**

```bash
nmap scan-options target(s)
```

eg:

```bash
nmap -F 192.168.1.1-253
```
