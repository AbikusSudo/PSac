# PSac — Passive Scale Access Circuit
# by AbikusSudo!!

### PSac (Passive Scale Access Circuit) is a passive and scalable access mechanism designed to keep proxy subscriptions functional even under strict network filtering or whitelist-only environments. It ensures persistent accessibility by reusing known working endpoints and applying adaptive bypass rules.

# Overview

PSac does not actively modify traffic. Instead, it forms a passive access circuit by leveraging allowed network paths and previously resolved servers. When direct subscription updates become blocked, PSac reconstructs a functional configuration using archived endpoints and optional bypass parameters.

### Key Features

• Passive bypassing without active evasion
• Adaptive fallback using previously working servers
• Stable operation in white-list based networks
• Compatible with any link-based proxy format
• Optional bypass flag: PSacBypassRule=1
• Designed for long-term accessibility

### PSac Mechanism

A subscription is obtained at least once in a normal, unrestricted network.

Working servers are stored in a local archive.

When restrictions appear, PSac selects a functioning endpoint from the archive.

A new, valid proxy link is formed with an optional PSac bypass rule appended to the URI.

The user imports the resulting link in their client as usual.

## Sac Bypass Rule

The PSac bypass parameter enables compatibility with restricted networks:

?PSacBypassRule=1

It is appended to any configuration URI while keeping the original query intact.

### Example

A typical proxy link can be extended with PSac:

…&PSacBypassRule=1

This indicates that the configuration has been adapted using the PSac mechanism and is intended for restricted-network usage.

### Philosophy

PSac is built on three principles:
• Passive behavior
• Scalable fallback
• Continuous accessibility

It is not a separate protocol but rather a method of ensuring reliable access through reconstruction, adaptation, and preservation of known good paths.

### Credits

Developed and written by AbikusSudo only!
