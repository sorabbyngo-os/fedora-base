# Fedora inheritance

Sorabbyngo consumes Fedora bootc + RPM + systemd + SELinux.

- Image base: quay.io/fedora/fedora-bootc
- Package install: dnf using images/packages*.list
- Source reference trees: sources/ (bootc, ostree, rpm-ostree, selinux-*, …)
- We do not reimplement systemd or rpm; we vendor sources only for offline study/patching.

Pinned base: Fedora 45 (see `FEDORA_VERSION` in images/Containerfile).
