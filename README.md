# Check SMSEagle
Nagios/Icinga script to check NETGEAR devices

Used to check NETGEAR switches https://www.netgear.com

# Usage:
```
./check_netgear_switch -h [hostname] -c [community] -s [status]
```

# Options:
```
  -h [snmp hostname]	Hostname
  -c [community name]	community name (ex: public)
  -p [snmp port]	port for snmp request (default: 161)
  -P [port]		port to check
  -n [number of ports]	number of physical ports on device
  -o [options]		additional options
    d				only ports that are down (or anything except up)
    u				only ports that are up
  -s [check]		Check to be executed
    info			System infos
    port			Check status specific port ('P' option)
    ports			Listing of ports ('n' option defines number of port to check)
    uptime			System uptime
  -t [timeout]		duration before doing an timeout in seconds - default 10s
```

# Examples:
```
  ./check_netgear_switch -h 1.2.3.4 -c public -s info
  ./check_netgear_switch -h 1.2.3.4 -p 4321 -c public -s uptime -t 30
  ./check_netgear_switch -h 1.2.3.4 -c public -s ports -n 28
  ./check_netgear_switch -h 1.2.3.4 -c public -s port -P 1
```
