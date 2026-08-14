ip addr
ip route
ping
dig
ss
tcpdump 

# Linux Networking Commands for Network Engineers

This document contains Linux networking commands I'm practicing as I
expand my Cisco networking background into Linux systems and network
automation.

The objective isn't simply to memorize commands. Each command should
answer a troubleshooting question.

## 1. ip addr

### Question

Does the server have the IP configuration I expect?

### Command

```bash
ip addr 

What I'm Looking For
Interface state
IPv4/IPv6 addresses
Subnet/prefix length
Expected interface

Question
Does the server know where to send traffic?
ip route
This is conceptually similar to inspecting the routing table on a
router.
default via 192.168.1.1 dev ens192
192.168.1.0/24 dev ens192 proto kernel
ping -c 4 192.168.1.1

I can use this progressively:
Test the local gateway
Test a remote IP
Test a hostname

Those results help distinguish local connectivity, routing, and DNS
problems.

And continue through the ten commands.

That's substantially better GitHub content than:

HERE ARE TEN COMMANDS
because it demonstrates how you think.
