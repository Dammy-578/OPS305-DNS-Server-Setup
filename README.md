# OPS305-DNS-Server-Setup
Secure DNS server deployment on AWS EC2 with primary/secondary zone files, firewall controls using nftables, and subnet-based traffic rules. Completed for OPS305 at Seneca Polytechnic.
# Primary & Secondary DNS Server Setup – OPS305 Assignment

**Course:** OPS305 – Linux Server Administration  
**Date:** October 2024  
**Institution:** Seneca Polytechnic

---

## 🧠 Overview
This project involved configuring and securing a DNS system in AWS using two EC2 instances. One acted as a primary server, the other as a secondary, both providing forward and reverse lookups for custom domain zones. Security was implemented using nftables with strict traffic controls.

---

## 🛠️ Project Features
- Configured BIND9 on Ubuntu with custom DNS zones (`assign.ops.fwd`, `assign.ops.rev`)
- Set up primary (`alnilam`) and secondary (`alnitak`) DNS roles
- Enabled zone transfers with timed synchronization (every 4 days)
- Applied `nftables` firewall rules to:
  - Permit DNS traffic only from allowed subnets
  - Allow ICMP (ping) only from the assignment subnet
  - Enforce default drop policy for all other traffic

---

## 🔐 Security Focus
- nftables rules load on boot
- Strict access via AWS Security Groups + internal firewall
- DNS query restriction by subnet

---

## 🧠 Skills Demonstrated
- DNS Configuration (BIND9)  
- Linux Firewall Management (nftables)  
- AWS EC2 Networking  

---

## ✅ Project Status
- ✔️ DNS zones working for forward & reverse lookups  
- ✔️ Zone transfers between primary and secondary servers  
- ✔️ nftables firewall rules enforced and validated
