![Python](https://img.shields.io/badge/Python-v3.11.x-FFD43B) ![RHEL](https://img.shields.io/badge/RHEL-v9.x-CC0000) ![AWS-EC2](https://img.shields.io/badge/AWS-EC2-FF9900) ![AWS-OpenSearch](https://img.shields.io/badge/AWS-OpenSearch-11009E)


# System Monitoring and Alerting using Python, AWS EC2, OpenSearch

## Overview
This project implements a monitoring and alerting system to track CPU utilization on AWS EC2 instances and generate alerts when predefined thresholds are exceeded. It demonstrates how production systems can be monitored in real time and how alerts can be triggered for proactive issue resolution.

## Features
- Remote monitoring of EC2 instances using SSH (Paramiko)
- CPU utilization tracking using Linux system commands
- Threshold-based alerting mechanism
- Integration with AWS OpenSearch for alert storage and querying
- Automated alert report generation
- Simulation of high CPU load for testing monitoring behavior

## Tech Stack
- Python
- AWS EC2 (RHEL)
- AWS OpenSearch
- Paramiko (SSH connection)
- OpenSearchPy (client library)

## How It Works
1. Establishes a secure SSH connection to an EC2 instance.
2. Executes system-level commands to fetch CPU usage.
3. Continuously monitors CPU metrics at regular intervals.
4. Triggers alerts when CPU usage exceeds a defined threshold.
5. Stores alert data in OpenSearch for analysis.
6. Generates a report file (`alert_report.txt`) with alert details.

## Usage
- Run the Python script.
- Provide required inputs:
  - EC2 hostname
  - Username
  - Private key path
  - OpenSearch host and credentials
- The script will:
  - Simulate high CPU load
  - Monitor system performance
  - Generate alerts when thresholds are exceeded

## Customization
- **Threshold**: Modify CPU alert threshold in the script (`if cpu_usage > value`)
- **Monitoring Interval**: Adjust sleep duration in loop
- **CPU Load Simulation**: Modify `stress-ng` command parameters

## Use Case
This project simulates real-world production support scenarios where system performance monitoring and alerting are critical for maintaining application reliability and preventing downtime.

## Notes
- Requires access to an AWS EC2 instance and OpenSearch domain
- Ensure proper SSH permissions and credentials are configured
- Designed for learning and demonstrating monitoring workflows

# Contributing
Contributions are welcome! If you have any improvements, bug fixes, or additional examples related to Monitoring Logs and Generating Alerts using Python, feel free to open a pull request. Please ensure your contributions adhere to the repository's coding standards and include relevant documentation.
