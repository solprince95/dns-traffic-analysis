
# 🛡️ DNS Traffic Capture with tcpdump (Kali Linux)

## 📘 Overview

This project demonstrates how to capture DNS traffic using `tcpdump` inside Kali Linux, analyze it with Wireshark, and identify basic DNS behavior.

I visited a cake recipe website from the Kali VM and captured real DNS queries, showcasing what domain lookups look like at the packet level.

---

## 🧰 Tools Used

- Kali Linux (running in VirtualBox)
- Firefox (to generate DNS traffic)
- tcpdump (packet capture tool)
- Wireshark (for .pcap analysis)
- Windows shared folder (for file transfer)

---

## 🧪 Lab Steps

1. Opened terminal in Kali
2. Ran `sudo tcpdump -i eth0 port 53 -w dns-capture.pcap`
3. Opened Firefox and visited `yummyrecipesforme.com`
4. Stopped capture with `Ctrl + C`
5. Moved the `.pcap` file to Windows using a shared folder
6. Opened and analyzed the file in Wireshark

---

## 🔍 Sample Output (from terminal)

IP 192.168.1.15.52943 > 8.8.8.8.53: 34567+ A? yummyrecipesforme.com. (35) IP 8.8.8.8.53 > 192.168.1.15.52943: 34567* 1/0/0 A 93.184.216.34 (51)

---

## 🎯 What I Learned

- DNS uses UDP port 53
- How `tcpdump` can capture real-time packets
- DNS query format: `A? domain.com`
- How to read `.pcap` files in Wireshark
- File transfer from Kali to Windows via shared folders

---

## 📁 Files Included

- `dns-capture.pcap` – Packet capture file of DNS queries
- `README.md` – Project documentation

---

## ✅ Created as part of my Cybersecurity Lab Portfolio

Certificate: Google Cybersecurity Professional Certificate  
Platform: Kali Linux in VirtualBox
