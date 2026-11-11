# Testing Automation Developer

If you can do the majority of the below, and learn the rest, we want to hear from you! Don't be put off if you don't tick all the boxes!

## The Role

Every layer of our stack works fine on its own. Making them all work together - in the field, over unreliable cellular links, under load, when things go wrong - is where the interesting problems live. We need someone to build the automated test harnesses that prove that end to end. Not "add unit tests to legacy code": the real work is chaos engineering, integration testing across the stack, and simulating field failures in a repeatable way.

You'll partner tightly with the QA/QC Engineer we're hiring alongside - they find the failure modes manually, you turn them into permanent regressions.

Our stack is distributed by design: config changes reach routers on eventual-consistency loops, drift reconciliation, routers and cloud infra exchange state asynchronously, and cellular introduces its own unpredictability underneath. Testing this well means understanding state convergence, cycle-aware assertions, and the difference between "the system settled to the right answer" and "the system happens to look right at this exact moment".

## What You'll Do

- Build integration test harnesses that exercise end-to-end integration tests across hardware and cloud. Hardware-in-the-loop where it matters; containerised simulators where it doesn't
- Design and run chaos experiments regularly: kill a cloud service mid-session, force a wrong APN, corrupt an OTA, restart a bonding subflow at a random moment, saturate a link, fail a DTLS handshake, delay a Portal poll cycle
- Instrument the bonding engine (Rust) with the assertions and fault-injection points needed to run the above deterministically
- Build automated tests for the router-side code where none currently exist. Focus on bonding, thermal, config-application, OTA updating and resilience
- Own CI-side testing for the Management Portal (React + Go): API contract tests, RBAC boundary tests across the six role tiers, end-to-end UI tests, load tests for the config-push pipeline
- Build integration tests using Docker-based test environments
- Test real-time features - SSE event streams end to end
- Build the Terraform test suite: linting, plan-diff review, cross-region smoke tests, teardown correctness
- Wire everything into GitHub Actions so failures block merges and page whoever's on the ticket
- Own flaky-test triage - either fix the underlying bug or delete the test

## Required Skills

- Strong programming background in at least one systems language (Rust, Go, or C) plus a scripting language (Python or shell)
- Substantial experience building test *infrastructure*, not just writing tests - fixtures, harnesses, hardware control loops, environment orchestration
- Experience testing distributed systems - understanding eventual consistency, state convergence, and how to write assertions that account for propagation windows without becoming flaky
- Test automation frameworks (Go testing, Jest, Playwright, or similar)
- CI/CD fluency - GitHub Actions or similar. Caching, matrix builds, secrets, self-hosted runner topology
- Docker for test environment orchestration
- Networking depth: TCP/UDP, tunnels, NAT, multi-path routing, DNS - including what a broken MTU looks like on the wire

## Technical Knowledge

- Go testing patterns and table-driven tests
- React component and end-to-end testing
- Performance and load testing
- Security testing fundamentals - including mTLS and certificate-based auth
- SQL and database testing
- Real-time event stream testing (SSE)
- Mock server and test fixture design
- Property-based testing, fuzzing, differential testing - techniques for shaking out edge cases example-based tests miss

## Nice to Have

- Rust test frameworks (`cargo test`, `criterion`, `proptest`)
- Chaos-engineering tooling (Chaos Mesh, Toxiproxy, `tc netem`, custom equivalents)
- Prior work testing OpenWRT or another embedded Linux distro - building images, packaging tests into a rootfs overlay, running under qemu
- Cellular test rigs - SIM emulators, RF chambers, cellular network simulators
- Terraform testing tools (`terratest`, `tflint`, `checkov`)
- Infrastructure testing at scale

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
