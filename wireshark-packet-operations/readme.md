# TryHackMe - Wireshark: Packet Operations (Write-up)

## Goal
Practice Wireshark filtering and protocol analysis:
- Statistics views (IPv4/IPv6, DNS, HTTP)
- Display filters (IP/TCP/UDP/HTTP/DNS)
- Advanced operators (contains, matches, in, string)
- Profiles (Checksum Control)

## Environment
- Platform: TryHackMe
- Tool: Wireshark
- Capture: `Exercise.pcapng`

---

## Key Concepts Learned
### Capture vs Display Filters
- **Capture filters**: set before capture, hard to change, risk missing traffic
- **Display filters**: used during/after capture, flexible, best for investigation

---

## Useful Filters (Cheat Sheet)

### IP / TTL
```wireshark
ip
ip.addr == 10.10.10.111
ip.src == 10.10.10.111
ip.dst == 10.10.10.111
ip.ttl < 10
