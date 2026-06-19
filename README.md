# *bedrock*

A playbook of the architectural root of my security model. It defines the foundational layers, principles and controls that every system must satisfy before it can be considered trusted.

## *The Defense-in-Depth Model*

Security is executed sequentially from the absolute core hardware outward to the network edge. If a lower layer is compromised, the integrity of all layers above it is void.

```text
[ Layer 7: Aliasing ] --- Identity
    [ Layer 6: Data ] --- Master Vault, TOTP
        [ Layer 5: Gateway ] --- Browser, Search Engine
            [ Layer 4: Network ] --- Router, Firewall, DNS
                [ Layer 3: Data at Rest ] ---  Storage
                    [ Layer 2: Compute ] --- Operating System
                        [ Layer 1: Core ] --- Firmware/UEFI
```
