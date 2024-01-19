# README for Multiple Website Certificates Monitoring with Zabbix Agent 2

## Overview
This Zabbix template is designed to monitor multiple SSL/TLS certificates on a single server using Zabbix Agent 2. It allows for the efficient tracking of certificate validity and notifies you before they expire.

## Features
- Monitors multiple SSL/TLS certificates.
- Easy to configure for various websites hosted on the same server.
- Provides alerts before certificate expiration.

## Requirements
- Zabbix Server (version 6.4 or later).
- Zabbix Agent 2 installed on the server where certificates are hosted.

## Installation
1. Download the YAML template file.
2. Log in to your Zabbix frontend.
3. Go to Data collection -> Templates.
4. Click on the “Import” button.
5. Upload the downloaded YAML file and import it.

## Configuration
1. Add the template to the host you want to monitor in Zabbix.
2. Configure the macro `{$CERT.WEBSITE.HOSTNAME}` with a comma-separated list of URLs whose certificates you want to monitor.
   - Example: `https://example1.com,https://example2.com`
3. Ensure Zabbix Agent 2 is correctly configured and running on the target server.

## Usage Example
After successful installation and configuration, Zabbix will start monitoring the SSL/TLS certificates of the specified URLs. You can view the status of these certificates in the Monitoring -> Latest data section of your Zabbix frontend.

The template triggers alerts based on the certificate expiry, ensuring that you are notified in advance to take necessary actions.

## Support
For issues, suggestions, or contributions, please use the GitHub repository's issue tracker or submit a pull request.
