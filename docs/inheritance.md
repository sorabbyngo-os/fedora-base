# Fedora inheritance

Sorabbyngo consumes Fedora bootc + RPM + systemd + SELinux.

- Image base: quay.io/fedora/fedora-bootc
- Package install: dnf using images/packages*.list
- Source reference trees:
  - Boot: sources/boot/
  - Init: sources/init/
  - Packaging: sources/packaging/
  - Security: sources/security/
  - Compositors: sources/compositor/
  - Display protocols: sources/display/
- We do not reimplement systemd or rpm; we vendor sources only for offline study/patching.

Pinned base: Fedora 45 (see `FEDORA_VERSION` in images/Containerfile).

## Smithay source policy

- Vanta currently uses the standalone Smithay 0.7.0 checkout at `../smithay`.
- Vendored reference: `sources/compositor/smithay/`.
- The vendored snapshot has different Calloop, Winit, and X11rb dependency versions.
- Do not switch Vanta to the vendored snapshot until compatibility and workspace tests pass.
- Preserve both copies until the migration is validated.
