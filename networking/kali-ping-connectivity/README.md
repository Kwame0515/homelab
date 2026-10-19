# Kali Linux — Network Connectivity and Interface Testing

## Objective
Test connectivity from a Kali Linux virtual machine to an external IP address and another lab machine, and inspect the VM's network interface configuration.

## Environment
- Kali Linux terminal
- Local lab target: `192.168.213.130` (identified as Metasploitable in the screenshot filename)
- Public test IP: `8.8.8.8`

## Tests and observations

### 1. External connectivity
Command: `ping 8.8.8.8 -c 4`

- Four ICMP echo requests sent and four replies received.
- **0% packet loss**.
- Average round-trip time: **35.289 ms**.

This demonstrates successful ICMP connectivity to the public test address at the time of testing.

### 2. Interface configuration
Command: `ifconfig`

- Interface: `eth0`
- IPv4 address: `172.16.98.129`
- Netmask: `255.255.255.0`
- Interface flags include `UP` and `RUNNING`.
- Loopback interface: `lo` with `127.0.0.1`.

The screenshot demonstrates inspection of the VM's assigned network address and active interfaces.

### 3. Local lab connectivity
Command: `ping 192.168.213.130 -c 4`

- Four ICMP echo requests sent and four replies received.
- **0% packet loss**.
- Average round-trip time: **1.481 ms**.

This demonstrates that the local lab IP was reachable over ICMP at the time of testing. It does not, by itself, verify the target operating system or any specific open ports.

## Commands practiced
```bash
ping 8.8.8.8 -c 4
ifconfig
ping 192.168.213.130 -c 4
```

## Skills demonstrated
- ICMP network connectivity testing
- Interpreting packet loss and latency
- Identifying an IPv4 address and subnet mask
- Inspecting virtual network interfaces
- Basic connectivity troubleshooting in a Linux VM

## Key takeaway
A successful ping indicates that ICMP echo replies reached the source. Combined with interface inspection, this is a useful first step in troubleshooting VM network connectivity. More tests are required to confirm DNS, application access, or open ports.

## Screenshots
Two screenshots were supplied: **Kali (ifconfig:ping).png** and **Kali (Ping metasploitable).png**. Their observations are documented above; the image files themselves have not yet been committed to this repository.
