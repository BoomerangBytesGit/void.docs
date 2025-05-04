# Router/Firewall

This is the main entry & exit point of all traffic.

We use OPNsense for this, you can find the documentation here: https://docs.opnsense.org/

## Keeping secure

You should update at least every month, better yet weekly, due to security this cannot be automated at this time:
Directions: System->Firmware->Status->Check For Updates
At path: /ui/core/firmware#status

## Threat Detection

All traffic is ran through various checks for malicious traffic both before & after connection. It is ran both for internet & local traffic (WAN/LAN IN/OUT), it does not run for the honeypot network (DMZ) by design, which has its own logging.

What we have deemed malicious traffic is blocked & others are set to just alert. For performance & network stability not every rule is enabled, And fewer to drop. You will want to fine tune these policies to your use case.

On default after connection its set to aggressively block all traffic from known malicious IPs & any rules that match Critical/Major severity + High confidence. For a total of 166,509 rules. This does not include the several other enabled plugins that handle threats.

This however can be adjusted to block more or less, block too much or the wrong things and you may have trouble running normal applications.

### Please read before modifying rules:

1. Please only use policies to modify rules, don't use the specific rules themselves.
2. Research the rules & the possible selectors for policies before enabling/disabling

drop = Blocks connection
alert = Log the rule when triggered
rule = Individual rule for a single threat
ruleset = A collection of rules for a specific use case
deprecated/deleted = Rules that no longer (or shouldn't be) used

### Paths to modify threat detection policies

You can view the ruleset list:
Dir: Services->Intrusion Detection->Administration->Download
Path: /ui/ids#download_settings

You can view/browse rules:
Dir: Services->Intrusion Detection->Administration->Rules
Path: /ui/ids#rules

You can modify the rules safely using policies:
Dir: Services->Intrusion Detection->Policy->Policies
Path: /ui/ids/policy#policies

We use clam-av for anti-virus, configure it here:
Dir: Services->ClamAV->Configuration
Path: /ui/clamav/general/index

Can modify lists for blocking threats before connection here:
Dir: Services->Unbound DNS->Blocklist
Path: /ui/unbound/dnsbl/index



