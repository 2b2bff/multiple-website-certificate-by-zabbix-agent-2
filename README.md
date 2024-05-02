
# Multiple Website certificate by Zabbix agent 2

## Description

This template allows you to monitor multiple TLS/SSL certificates on a single host by Zabbix agent 2 without any external scripts.

## Requirements
 - Zabbix 6.0 or higher

## Setup

1\. Download the template and import it to Zabbix.

2\. Create a host for the TLS/SSL certificates with Zabbix agent interface.

3\. Link the template to the host.

4\. Customize the value of {$CERT.WEBSITE.LIST} macro.

## Zabbix configuration

No specific Zabbix configuration is required.

### Macros used

|Name|Description|Default|Example|
|----|-----------|-------|-------|
|{$CERT.WEBSITE.LIST}|Array of elements - hostname(:port(:IP)) where each host is delimited by a comma.||`<hostname1>[:<port1>[:<ip1>]],<hostname2>[:<port2>[:<IP2>]], ...`|
|{$CERT.EXPIRY.WARN}|Number of days until the certificate expires.|7|30|
|{$CERT.WEBSITE.IP}|Default IP address.|||
|{$CERT.WEBSITE.PORT}|Default TLS/SSL port.|443||
