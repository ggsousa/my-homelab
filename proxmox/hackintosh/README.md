# 🍎 Native Hackintosh Build: macOS Sequoia 15.7.3

This folder documents my native (bare metal) Hackintosh setup. This is my secondary workstation, built on the Intel HEDT (High-End Desktop) platform for stability and macOS testing.

## 🖥️ Hardware Specifications
- **CPU**: Intel Core i7-7820x (Skylake-X) overclocked to 4.5 - 4.8GHz.
- **Motherboard**: AORUS X299 Gaming 7.
- **GPU**: ASUS Radeon RX 580 8GB (Native OOB support).
- **Memory**: 32GB (4x8GB) DDR4 3200MHz.
- **OS**: macOS Sequoia 15.7.3 (Dual boot with Windows 11).

## 🛠️ Build Details
- **Bootloader**: OpenCore.
- **Platform ID**: iMacPro1,1 (even the sequoia) or MacPro7,1 (Tahoe).
- **Storage**: Dedicated 360GB SATA SSD, NVMe 512GB Windows 11.

## 🔧 X299 Specific Configuration
Running macOS on X299 requires specific attention to:
- **TSC Sync**: Using `CpuTscSync` to prevent kernel panics on multi-core Skylake-X CPUs.
- **ACPI Patches**: Custom SSDTs for RTC, HPET, and USB mapping (essential for X299).
- **MSR 0xE2**: BIOS is unlocked to allow native power management without `AppleCpuPmCfgLock`.

---
> **Note**: This setup is for educational purposes. Always refer to the [Dortania OpenCore Guide](https://dortania.github.io/OpenCore-Install-Guide/) as your primary source of truth.
