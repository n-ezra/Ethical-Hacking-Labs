# Email Harvesting using theHarvester

## Overview

This project demonstrates email harvesting and passive reconnaissance techniques using theHarvester tool. The objective is to gather publicly available email addresses, subdomains, hosts, and employee-related information associated with a target domain through OSINT techniques.

## Tool Used

* theHarvester

## About theHarvester

theHarvester is an open-source OSINT reconnaissance tool used for gathering:

* Email addresses
* Subdomains
* Employee names
* Hosts
* IP addresses

from publicly available search engines and data sources.

## Installation

### Kali Linux

```bash id="lb3qv8"
sudo apt install theharvester
```

### GitHub Installation

```bash id="3q0rbn"
git clone https://github.com/laramies/theHarvester.git
```

## Basic Syntax

```bash id="n8ejmz"
theHarvester -d example.com -b google
```

## Practical Commands

### Google Search Engine

```bash id="crnhiv"
theHarvester -d example.com -b google
```

### Bing Search Engine

```bash id="tdw3w3"
theHarvester -d example.com -b bing
```

### LinkedIn Enumeration

```bash id="z0br1f"
theHarvester -d example.com -b linkedin
```

### Multiple Data Sources

```bash id="63eqv7"
theHarvester -d example.com -b all
```

## Sample Output

The tool successfully gathered:

* Public email addresses
* Subdomains
* Related hosts
* Employee information

## Screenshots

Add screenshots inside the `/screenshots` folder:

* Tool installation
* Command execution
* Harvested results

## Learning Outcomes

* Passive reconnaissance
* OSINT methodology
* Email harvesting techniques
* Search engine reconnaissance
* Information gathering

## Disclaimer

This project is intended strictly for educational and ethical cybersecurity learning purposes. All testing was performed only on authorized or publicly available targets.
