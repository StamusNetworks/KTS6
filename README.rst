===============================
Kibana 6 Templates for Suricata
===============================

Templates/Dashboards for Kibana 6 to use with Suricata IDPS threat hunting and the ELK 6 stack

This repository provides 17 templates for the Kibana 6.x and Elasticsearch 6.x
for use with Suricata IDS/IPS/ - Intrusion Detection, Intrusion Prevention and Network Security Monitoring system

These dashboards are for use with Suricata 4.1+ and enabled Rust build, Elasticsearch, Logstash, 
Kibana 6 and comprise of more than 170 visualizations and 15 searches.

The dashboards are:

 - SN-SMB
 - SN-IKEv2
 - SN-ALERTS
 - SN-ALL
 - SN-DNS
 - SN-FILE-Transactions
 - SN-FLOW
 - SN-HTTP
 - SN-IDS
 - SN-OVERVIEW
 - SN-SMTP
 - SN-SSH
 - SN-STATS
 - SN-TLS
 - SN-VLAN
 - SN-TFTP
 - SN-DHCP


How to use
==========

::

     apt-get install git-core
     git clone https://github.com/StamusNetworks/KTS6.git
     cd KTS6
     
Load the dashboards: ::

 ./load.sh

 
You would need to select ``logstash-*`` as a default index once you open any dashboard for the first time after initial load/import.

For optimal results an example of elasticsearch template has been included under `es-template\elasticsearch6-template.json` that is used in SELKS 5.

**NOTE:**  
This will delete any custom dashboards you already have in place. 

**NOTE:**  
In order to use the full HTTP logging dashboard template you need to set up Suricata as
explained here - http://www.pevma.blogspot.se/2014/06/http-header-fields-extended-logging.html  

**NOTE:**  
If the traffic you are inspecting contains vlans - in order to use the VLAN template, make sure you have enabled vlan tracking in ``suricata.yaml`` -

     vlan:
       use-for-tracking: true

**NOTE:**  
For best user experience use with 1680 x 1050 screen resolution!!  

Do not hesitate to test,feedback and contribute !
