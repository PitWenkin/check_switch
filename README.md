# Check SMSEagle
Nagios/Icinga script to check NETGEAR devices

Used to check NETGEAR switches https://www.apc.com

# Usage:
```
./check_apc_ups -h [hostname] -c [community]
```

# Options:
```
  -h [snmp hostname]	Hostname
  -c [community name]	community name (ex: public)
  -p [snmp port]	port for snmp request (default: 161)
  -t [timeout]		duration before doing an timeout in seconds - default 10s
```

# Examples:
```
  ./check_apc_ups -h 1.2.3.4 -c public 
  ./check_apc_ups -h 1.2.3.4 -p 4321 -c public -t 30
```
