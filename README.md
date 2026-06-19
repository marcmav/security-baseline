# *bedrock*

A playbook of the architectural root of my security model. It defines the foundational layers, principles and controls that every system must satisfy before it can be considered trusted.

## *The Defense-in-Depth Model*

Security is executed sequentially from the absolute core hardware outward to the network edge. If a lower layer is compromised, the integrity of all layers above it is void.

```text
[ Layer 6: Gateway ] --- Web Browser (Firefox), Search, Aliasing
    [ Layer 5: Network Edge ] ─── Router, UFW Firewall, DNS (NextDNS)
        [ Layer 4: Compute ]   ─── OS (Arch Linux/Hyprland), Kernel Hardening
            [ Layer 3: Storage ]   ─── LUKS2 Full-Disk Encryption, Partitioning
                [ Layer 2: Identity ] ─── Master Vault, TOTP, Hardware Keys
                    [ Layer 1: Core ]     ─── Firmware/UEFI, Hardware, OpSec

