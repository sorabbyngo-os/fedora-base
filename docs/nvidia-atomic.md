# NVIDIA on Fedora bootc / Atomic

Use RPM Fusion, not Pop!_OS debs.

1. Enable RPM Fusion on the image build or first boot.
2. Install: akmod-nvidia, xorg-x11-drv-nvidia, optionally xorg-x11-drv-nvidia-cuda
3. Kernel args: rd.driver.blacklist=nouveau modprobe.blacklist=nouveau nvidia-drm.modeset=1
4. Secure Boot: enroll MOK for akmods when required.
