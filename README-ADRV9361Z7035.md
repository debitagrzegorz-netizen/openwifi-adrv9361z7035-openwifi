# ADRV9361-Z7035 port branch (`adrv9361z7035-2025.1`)

This branch carries the openwifi driver and userspace changes for the
ADRV9361-Z7035 SOM on the ADRV1CRR-BOB carrier, built with Vivado and
PetaLinux 2025.1.

- Upstream: [open-sdr/openwifi](https://github.com/open-sdr/openwifi)
- Base commit: `f6674ee` (upstream `master`, "Merge pull request #498 from robgar2001/nlnet")
- Integration repository (build scripts, PetaLinux layer, tests, release
  notes): [openwifi-adrv9361z7035](https://github.com/debitagrzegorz-netizen/openwifi-adrv9361z7035)
- Release tags: `adrv9361z7035-2025.1-v1.1` and `adrv9361z7035-2025.1-v1.2`
  (both `08827d5`)

Port commits on top of the base:

- `e3d17b9` Keep TX completion off `priv->lock` on the ADRV9361 port.
- `75ab6fe` Fix side_ch reload on kernel 6.12.
- `54e77c2` Fix the TX lost wake and recover a frozen FPGA TX queue in the driver.
- `08827d5` Retire orphaned TX BDs in the watchdog and expose the TX ring state.

Licence: as upstream (AGPL-3.0, with the upstream dual-licence note).
