# QA/QC Engineer

If you can do the majority of the below, and learn the rest, we want to hear from you! Don't be put off if you don't tick all the boxes!

## The Role

We're looking for a QA/QC Engineer to be the person who tries to break everything. Every release, every feature, every hardware SKU. You'll design failure scenarios and run them against real hardware, verify Management Portal changes actually reach and apply on routers, and find the ugly failure modes before customers do.

## What You'll Do

- Find the edge cases, be the equivalent of 'a man walks into a bar and orders -2 beers'
- Own the end-to-end test plan for each release across the four product surfaces: router firmware, bonding engine, Management Portal and cloud infra.
- Design and run failure scenarios against real hardware: pull SIMs, cover antennas, brown-out the power, saturate the LAN, drop a carrier mid-call, roam across cell boundaries with a moving test rig, spike modem temperatures until thermal fallback kicks in
- Verify Management Portal config changes actually reach and apply on routers, and that the config-drift reporter behaves under contention
- Test the sad paths: expired certificates, revoked certificates, mismatched firmware images, corrupted OTA downloads mid-flight, orphaned Exit Node routes, malformed Management Portal inputs, RBAC boundary probing across all role tiers
- Test the ugly paths: SIMs quietly deprioritised at peak, cell towers that misreport signal, cloud infra routing tables, DNS failures that mask as bonding failures
- Perform security testing and vulnerability assessments across backend, frontend, and device firmware
- Reproduce customer-reported issues on the bench with a matched hardware config, then document the reproduction so engineering can build a regression
- Own the QA pass gate for hardware - the "Passed QA" lifecycle status only moves forward when you say so
- Define and track quality metrics; feed everything you find back into the automated test suite and to the Support function

## Required Skills

- Several years testing networking, embedded, or distributed systems in production environments
- Comfortable at the Linux shell - reading logs, writing small scripts, using `tcpdump`, `iproute2`, `iptables`, systemd journals
- TCP/IP, DHCP, routing, VPN tunnels, NAT, DNS - enough to tell when a symptom is a network issue vs a code issue
- Cellular basics - SIMs, APNs, LTE vs 5G NR, RSRP/RSRQ/SINR, cell attach behaviour, carrier priority
- Ruthless about reproduction: a bug isn't real until you can make it happen twice with a written recipe
- Written communication that a support engineer three months from now will thank you for

## Technical Knowledge

- Test-plan design for microservices and distributed systems
- API testing (REST, authentication flows, mTLS + JWT)
- Certificate and TLS testing
- Real-time event stream testing (SSE)
- Security testing fundamentals - OWASP-adjacent, RBAC boundary probing
- Network protocol testing and packet capture analysis
- Test fixture and mock-server design

## Nice to Have

- Prior work with OpenWRT, LEDE, or similar embedded Linux distros
- Prior work with bonded / multipath transports (MPTCP, Speedify, Peplink, custom)
- Field-service background - you've been the person on-site fixing a broken deployment at 2am
- Familiarity with test hardware you didn't build yourself: RF chambers, cellular emulators, Faraday enclosures
- Terraform, Ansible, or similar IaC exposure - enough to spin up test infrastructure without needing a DevOps handover
- Chaos engineering principles

---

## How we work

### High ownership

Every team member owns their work end to end. Accountability from first thought through shipped, deployed, and monitored - no throw-it-over-the-wall.

### Resourcefulness

Small teams solve problems by being creative with what's in front of them. The best fix is often the one you can start today with the tools already on your bench.

### Collaboration

We work in the open. Anyone can review anyone's code, every decision is discussable, and we combine backgrounds - networking, embedded, cloud, front-end - because that's what the stack needs.

### Excellence

We hold high standards for what we ship. Our customers rely on connectivity that has to work - "try again later" isn't an option on a live broadcast or a moving vehicle.

### Innovation

Bonded 4G/5G is a demanding field with a small number of serious players. Staying ahead means constantly pushing what's possible - new hardware, better bonding, tighter operational insight. If you like frontier work, this is that.

---

[Back to all positions](../README.md)
