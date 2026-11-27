# panzio-halozat.
**panzió** hálózat *Packet tracerben* szimuláltuk.

## Eszközök
- R0: panzió
- R1: szolgáltató
- R2: kávézó

  [Cisco Packet Tracer](https://www.netacad.com/cisco-packet-tracer)

## Címzés

| Hálózat | Cím | Átjáró |
|---|---|---|
| Recepció (VLAN 10) | `192.168.10.0/24` | `192.168.10.1` |
| Vendég (VLAN 20) | `192.168.20.0/24` | `192.168.20.1` |
| Szerver (VLAN 30) | `192.168.30.0/24` | `192.168.30.1` |
| Kávézó | `192.168.40.0/24` | `192.168.40.1` |

## NAT beállítás

```
acess-list 1 permit 192.168.10.0 0.0.0.255
ip nat inside source list 1 interface g0/2 overload
```
