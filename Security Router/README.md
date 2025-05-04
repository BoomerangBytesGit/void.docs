# void.router
Information on how to maintain, debug & modify a void router

## What it is

Void router is a homebrewed security & (lesser so) privacy focused router. It prioritizes security above all else in a way you can heavily customize too your liking.

To break it down it is a KVM Hypervisor running heavily pre-configured & modified OPNsense with a Honeypot & includes a easy to use GUI directory with easy to follow documentation. You can keep it as simple or complex as you would like. For more complex control you can find the documentation to the components directly here:

https://docs.opnsense.org/
https://pve.proxmox.com/pve-docs/

It is a system meant for convenience, that offers much higher security than traditional routers. It is built for the paranoid or the less tech savvy, with options for support to extend the system to your specific use case.

## What it can do

It will protect you from a massive amount of threats, it can be better fine tuned for specific use-cases, at default it protects for a general user, but it can be configured to protect servers & their programs, block categories of sites (social media, NSFW, etc.), as restrictive as you like, privacy focused.

Our default configuration enforces the following:
- Active Anti-Virus
- AD Blocking
- Tracker Blocking
- Uses IPsec/CrowdSec for secure traffic exchange & active threat detection/blocking - Default collections + 15 general user orientated collections & custom rules
- Actively blocks 166,509 threats - With possibility to expand up to 227,993 or more with custom rulesets
- Restrictive firewall rules
- Blocks 11+ Lists containing 100K+ domains before DNS resolution/Connection
- DNS over TLS / DNS over HTTPS
- Uses only Quad9 privacy & security focused DNS servers - Malware filtering as primary & Non-Filtering as secondary
- Uses hardware passthrough
- Isolation between VMs
- Management only accessible via LAN
- Pre-configured router wide VPN setup for somewhat easy installation

## What we can do for you
- General support
- Set up/Integration of paid only features & security
- Set up a highly secure restrictive environment based on your specific use case
- Adapt to privacy focused - VPN, TOR, Proxy Integrations
- Set up paid IPsec advanced blocklists/whitelists

## Why doesn't it come with VPN/TOR/Proxy or any premium features
Due to Australian law we can't provide these services without greatly impacting you're security. We however can recommend the best solution, guide you through the account creation, subscriptions/purchases & implement the integration for you.

## What do you recommend for premium/paid/extra security/privacy?:
- Proxy: zenrows.com
- VPN: NordVPN
- Anonymity: TOR
- Premium Blocklists: crowdsec.net
- Advanced Threat Blocking (Replacement): Zenarmor
- Latest hypervisor updates: Proxmox Subscription
- + Many Others


