# Sorabbyngo OS — OS ONE 1.0 GNOME Pre-alpha

**Release channel:** Pre-alpha
**Edition:** GNOME
**Base:** Fedora 44 bootc
**Architecture:** x86_64
**Release date:** 2026-11-19

## Overview

OS ONE is the first Sorabbyngo OS release baseline. It establishes a Fedora-derived, image-based operating system with Sorabbyngo identity and a GNOME desktop.

The project retains Fedora's underlying bootc, RPM, systemd, kernel, SELinux and boot infrastructure. Sorabbyngo builds on that foundation rather than replacing those upstream systems.

## Included in this edition

- Fedora 44 bootc base.
- GNOME Shell and GNOME desktop session.
- GDM display manager.
- GNOME Settings, Files, Terminal, Software and Text Editor.
- NetworkManager Wi-Fi integration.
- Bluetooth, audio, power management and removable storage support.
- Firefox browser.
- Plymouth boot splash using the Sorabbyngo theme.
- Fastfetch configured with the original Sorabbyngo logo and OS ONE version.
- Sorabbyngo OS identity in os-release, login banners and system branding.
- Fedora SELinux policy and system infrastructure.

## Image-based operating model

The operating system is delivered as a bootc image.

- OS-level changes are built into and delivered through updated images.
- DNF is used during image construction.
- Flatpak is the intended application distribution route for desktop applications.
- Toolbx is intended for development environments.

## Scope and exclusions

This release focuses on the Fedora base, Sorabbyngo identity and GNOME desktop.

AION, Sentinel, HAL, Vanta and other custom Sorabbyngo components are not integrated into this release.

KDE, XFCE and COSMIC are planned as separate desktop editions sharing the OS ONE foundation. They are not included in this GNOME image.

## Validation

The OS ONE 1.0 GNOME image was built locally and exported as a QCOW2 disk image.

The QCOW2 image passed `qemu-img check` and was booted in the `os-one-gnome-dev` virtual machine. GNOME first-run setup completed, and the installed system displayed the Sorabbyngo Fastfetch logo and OS identity.

This is development validation, not a claim of production readiness or comprehensive hardware compatibility.

## Known status

This is a pre-alpha baseline. Hardware compatibility, installation workflows, upgrades, recovery, accessibility, security review and broader testing remain ongoing.

## Build identity

- Containerfile: `images/Containerfile`
- Fedora base version: `44`
- Image reference used for validation: `localhost/sorabbyngo-os:one-1.0-gnome`
- Validated image ID: `46836d838a78814b1bd0da2e5d6bb99471262973ef881e56efb4b1af53c7241a`
