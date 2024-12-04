# egress-check-range.nse
This Nmap NSE script tests egress filtering by attempting outbound connections to a specified external server across a range of ports.

## Usage
```
nmap <target-ip> --script egress-check-range --script-args "egress-server=<server-ip>,egress-ports=<start-end>"
```

## Requirements
The external server must have open ports to receive connections.

## Output
The script outputs the ports that allow outbound connections.

## Limitations
May require elevated privileges for certain port ranges.
