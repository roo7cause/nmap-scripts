# Egress Check NSE Script

## Purpose

The `egress-check.nse` script tests egress filtering by attempting to establish outbound connections from a target machine to an external server over a specified range of ports. This script helps network administrators and security analysts to:

- Identify which outbound ports are permitted by firewalls or network security policies.
- Validate egress filtering rules.
- Detect potential misconfigurations that could allow unauthorized exfiltration of data.

---

## Features

- Tests multiple ports within a user-defined range.
- Reports ports that allow outbound traffic to a specified external server.
- Configurable through simple arguments: `egress-server` and `egress-ports`.

---

## Example Usage

### Command Syntax
```
nmap <target-ip> --script egress-check --script-args "egress-server=<server-ip>,egress-ports=<start-<end>"
```

## Example Output
```
PORT     STATE SERVICE
22/tcp   open  ssh
111/tcp  open  rpcbind
443/tcp  open  https
631/tcp  open  ipp
5901/tcp open  vnc-1

Host script results:
|_egress-check: Egress allowed on ports: 22, 111, 443
```

