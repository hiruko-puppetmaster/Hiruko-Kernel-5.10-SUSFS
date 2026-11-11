<div align="center">

# Hiruko-Kernel-5.10-SUSFS

<img src="https://github.com/hiruko-puppetmaster/Hiruko-Kernel-5.10-SUSFS/blob/main/assets/e2da302e23220dd4807b8aa9a01de905.jpg" alt="Hiruko Banner" width="100%" style="border-radius: 6px;" />

> *"True art is an undying thing..."*

[![Kernel](https://img.shields.io/badge/Linux-5.10-blue?style=flat-square&logo=linux)](https://github.com/hiruko-puppetmaster/Hiruko-Kernel-5.10-SUSFS)
[![Android](https://img.shields.io/badge/Android-GKI-green?style=flat-square&logo=android)](https://android.googlesource.com/)
[![Root](https://img.shields.io/badge/KernelSU-%2B_SUSFS-red?style=flat-square&logo=shield)](https://gitlab.com/simonpunk/susfs4ksu)

</div>

---

### What is this?

This is my custom GKI 5.10 Android kernel build featuring built-in **KernelSU** and **SUSFS** patches. Built it to keep things running fast, stable, and hidden where it needs to be. 

If you're looking for a solid daily driver kernel that handles root hiding properly without messing up your system integrity checks, you're in the right place.

---

### Key Stuff Included

* **Base:** Linux Kernel 5.10 (GKI)
* **Root:** KernelSU / KernelSU-Next integration out of the box
* **Stealth:** SUSFS hooks patched in to handle mounts, hiding root strings, and passing device checks smoothly
* **Tweaks:** Cleaned up task scheduling and memory management for better battery and zero stutter while gaming

---

### Repo Layout

```text
Hiruko-Kernel-5.10-SUSFS/
├── arch/       # ARM64 architecture files
├── drivers/    # Custom drivers & sensor patches
├── kernel/     # Core kernel code & KSU hooks
├── fs/         # File systems + SUSFS implementation
└── build.config
```

---

### Quick Build Guide

Make sure you've got your toolchains set up on a Linux build machine, then run:

```bash
# Grab the source
git clone https://github.com/hiruko-puppetmaster/Hiruko-Kernel-5.10-SUSFS.git
cd Hiruko-Kernel-5.10-SUSFS

# Set arch
export ARCH=arm64
export SUBARCH=arm64

# Compile
make O=out your_device_defconfig
make -j$(nproc) O=out
```

---

### License

GPL v2. Check out the `COPYING` file if you want the boring legal details.
