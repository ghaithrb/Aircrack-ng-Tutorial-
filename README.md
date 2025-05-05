# Aircrack-ng Tutorial

## 🚀 Introduction

**Aircrack-ng** is a powerful suite of tools used for wireless network security auditing. It focuses on the detection of wireless vulnerabilities and cracking WEP and WPA-PSK keys.

## Author

Made by [Ghaithrb](https://github.com/ghaithrb)


## 📦 Features

- **WEP Cracking**: Crack WEP encryption using packet capture.
- **WPA/WPA2 Cracking**: Crack WPA and WPA2 passwords through dictionary attacks.
- **Packet Sniffing**: Capture packets from Wi-Fi networks.
- **Network Monitoring**: Monitor and analyze Wi-Fi traffic.

## 🔧 How to Use Aircrack-ng

### Installation

```bash
sudo apt-get install aircrack-ng
```

### Monitor Mode

- Enable Monitor Mode
  ```bash
  sudo airmon-ng start wlan0
  ```

- Stop Monitor Mode
  ```bash
  sudo airmon-ng stop wlan0mon
  ```

### Capture Packets

- Capture Packets
  ```bash
  sudo airodump-ng wlan0mon
  ```

- Capture WPA Handshake
  ```bash
  sudo airodump-ng --bssid [BSSID] -c [Channel] -w [Output File] wlan0mon
  ```

### WEP Cracking

```bash
sudo aircrack-ng -a 1 -b [BSSID] [Capture File].cap
```

### WPA Cracking (using dictionary)

```bash
sudo aircrack-ng -w [wordlist] -b [BSSID] [Capture File].cap
```

#### Dictionary Attack Example

```bash
sudo aircrack-ng -w /usr/share/wordlists/rockyou.txt -b [BSSID] [Capture File].cap
```

## 🛡️ Best Practices

- Only use Aircrack-ng on networks you own or have explicit permission to audit.
- Ensure you comply with local laws regarding wireless network security testing.
- Consider using Kali Linux or Parrot Security OS for a better Aircrack-ng experience.

## 📄 License

This tutorial is licensed under the MIT License. See the LICENSE file for details.
