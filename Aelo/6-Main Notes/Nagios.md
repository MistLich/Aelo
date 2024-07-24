
2024-07-23 16:22

Status : #baby 

Tags : [[Continuous Monitoring]] [[DevOps Tools]]

# Nagios

Nagios is an event monitoring system which offers monitoring and alerting services for servers, switches, applications and services. It alerts users when things go wrong and alerts them a second time when the problem has been resolved.

Nagios runs as a Daemon or service and periodically runs plugin on the same server and get status information. Nagios behaves like a scheduler that runs certain scripts and based on results take another action or run other scripts

ARCHITECTURE - server <--> agent architecture

Nagios server run on a host, and plugins interact with local resources or services or maybe even remote hosts or services. these plugins will send the info to scheduler, which will display in interface and if something goes wrong alert required users

NRPE - Nagios remote plugin executive usually for remote Linux/Unix machines


# References