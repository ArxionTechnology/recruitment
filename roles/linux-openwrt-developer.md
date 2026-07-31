# Linux / OpenWRT Developer

If you can do the majority of the below, and learn the rest, we want to hear from you! Don't be put off if you don't tick all the boxes!

## The Role

Our routers come in a variety of form factors depending on use case. All run a heavily customised OpenWRT build. 

You'll own the router-side Linux stack: keep the current shell + Lua + Python codebase reliable while gradually rewriting the load-bearing pieces in Go (or Rust where it fits), so the next generation is easier to test, easier to reason about, and cheaper to extend.

## What You'll Do

- Own the router-image build pipeline: OpenWRT source, our overlays, kernel config, package selection, per-SKU hardware variants.
- Develop and maintain OpenWRT firmware components - package creation, kernel configuration, and system integration
- Build device-side agents for metrics collection, configuration reconciliation, and secure device-to-cloud communication (mTLS)
- Take existing shell scripts and rewrite them in Go *where the change earns its keep* - long-running daemons, complex state machines, anything with concurrent I/O. Leave short shell utilities alone
- Design and maintain the on-router services: bonding subflow management, modem state, thermal fallback, config-application from the Portal, OTA update handling
- Integrate cellular modem APIs - signal metrics, bearer setup, network attach behaviour, AT-command sequences for modem control and diagnostics
- Work on VPN bonding and network optimisation features alongside the Rust bonding engine
- Keep the LuCI admin UI (Lua controllers + CBI models) working as OpenWRT versions advance. Extend it where field engineers need on-router visibility the Management Portal doesn't cover
- Debug the hard problems: modem firmware bugs, wireless driver quirks, USB modem enumeration races, ppp/qmi/mbim differences, netlink oddities
- Own kernel bumps, driver patches, occasional out-of-tree modules. Contribute upstream when a fix belongs there
- Partner with QA/QC and Testing Automation so changes are testable - no "works on my dev router"

## Required Skills

- Deep comfort with Linux userspace: procfs, netlink, `iproute2`, `iptables`/`nftables`, network namespaces, DHCP servers/clients, DNS resolvers, ppp/qmi/mbim modem stacks. Router side is OpenWRT running **procd** (not systemd); Management Plane / cloud infra run systemd - you'll touch both
- Solid Go - design a daemon that behaves correctly under signals and restarts; reason about goroutine leaks and context propagation
- Solid shell scripting - read a 400-line existing script, understand it, refactor confidently. Router side is BusyBox `ash`, not full bash; general shell fluency and awareness of the `ash` differences is what's needed
- Practical embedded Linux experience - OpenWRT, Yocto, Buildroot, or Debian on ARM
- C programming for low-level components and kernel-adjacent work
- Understanding of cellular networks - LTE/5G signal metrics (RSRP, RSRQ, SINR), bearer setup, carrier priority, and AT-command interaction with modems (with respect for how easily bad AT sequences can brick a modem)
- Networking depth end-to-end: routing tables, VPN tunnels, MTU, PMTUD, NAT, DNS behaviour under partial connectivity

## Technical Knowledge

- X.509 certificates and PKI, mTLS-based device-to-cloud auth
- Firmware update mechanisms - download, apply, verify, and the discipline that comes without a trivial rollback path
- Serial communication and device protocols
- Resource-constrained programming - routers have modest RAM and slow flash
- Hardware interfaces (GPIO, UART, SPI, I2C)
- Signal processing basics for cellular metrics

## Hardware Experience (Nice to Have)

- Prior OpenWRT / LEDE contribution - packages, ImageBuilder recipes, LuCI Lua modules, kernel patches
- Prior work with Wi-Fi drivers (`mac80211`, `hostapd`, `wpa_supplicant`) or cellular modem middleware (ModemManager, oFono, libqmi, libmbim)
- Kernel-side experience - reading and patching drivers, building custom kernels, debugging with printk/ftrace/kprobes/BPF
- Rust exposure - enough to work at the boundary with the bonding engine and contribute back to it when needed
- Debian packaging - `debhelper`, `.deb` build pipelines, dependency handling
- ARM SoCs, industrial single-board computers, or similar embedded hardware
- Hardware security modules (HSM, TPM)
- Embedded test rigs - serial consoles, JTAG, controlled reboots, network-boot for recovery

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
