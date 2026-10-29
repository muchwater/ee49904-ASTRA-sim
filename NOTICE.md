# Notice — third-party software and licenses

The starter kit in this repository installs and drives third-party open-source software. None of it
is redistributed here. Cite what you use, and read the license before you publish anything built on
it. `BRIEF.md` §7 has the details.

| Project | License | Redistributed here? |
|---|---|---|
| ASTRA-sim | MIT — its submodules differ, see below | no — cloned by `starter/setup.sh` |
| Chakra (MLCommons) | Apache-2.0 | no — ASTRA-sim submodule |
| Protocol Buffers | BSD-3-Clause | no |

**ASTRA-sim.** The simulator itself is MIT, but `setup.sh` fetches its submodules recursively and
they are not all MIT — the ns-3 network backend is **GPL-2.0**. This kit builds and uses the
analytical backend only, and nothing from any of them is redistributed here. If you publish code that
ships or links one of those backends, the license to respect is that submodule's, not ASTRA-sim's.

Everything in this repository is course material for KAIST EE49904 (Fall 2026),
© AI-Native Networking Lab, KAIST. Students enrolled in the course may clone it, modify it, keep
their own copies, and include the parts they used in the repository they submit with their report.
Redistribution beyond that, or reuse in another course, needs written permission.
