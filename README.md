# soc-splunk-monitoring-lab
SOC lab using Splunk to detect brute-force, SQL injection.
# SOC Monitoring Lab (Splunk)

## Overview
This project simulates a Security Operations Center (SOC) environment using Splunk to detect real-world cyberattacks.

## Architecture
Victim Machine (Ubuntu) → Logs → Splunk Forwarder → Splunk SIEM

## Attacks Simulated
- SSH Brute Force
- SQL Injection

## Detection Techniques
- SPL queries for pattern matching
- Regex-based field extraction
- Event correlation

## Example Query (Brute Force)
```spl
index=* "Failed password"
| rex "from (?<src_ip>\d+\.\d+\.\d+\.\d+)"
| stats count by src_ip

## Dashboard
The Splunk dashboard includes:
Brute-force monitoring
Web attack detection
Suspicious activity tracking

## Tools Used
Splunk Enterprise
Kali Linux
Ubuntu
