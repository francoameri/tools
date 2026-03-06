# ⚡ Quick Start Guide

## Step 1: Prepare the USB Drive
1. Download the latest **[Easy2Boot package](https://easy2boot-xyz.translate.goog/download/)** from the official site.
2. Insert your USB stick (16GB minimum recommended).
3. Run the Easy2Boot installer on a Windows system.
4. Choose the USB drive and let the installer format it with the required bootloader.

> Important note: Installing E2B can be quite complex, so here's a video from the author's website in case you need it:

[![E2B Install Process](https://img.youtube.com/vi/J7XjH-eLjbg/0.jpg)](https://www.youtube.com/watch?v=J7XjH-eLjbg)

## Step 2: Add ISOs
1. Copy ISO files directly to the Easy2Boot drive.
   - Place them in appropriate folders (`\_ISO\WINDOWS`, `\_ISO\LINUX`, `\_ISO\UTILITIES`).
2. No need to reformat or rebuild — just drag & drop.

## Step 3: Boot from USB
1. Plug the Easy2Boot drive into the target machine.
2. Enter BIOS/UEFI boot menu and select the USB drive.
3. Disable **Secure Boot** if enabled.
4. Choose the desired ISO from the Easy2Boot menu and boot.

## Step 4: Expand Your Toolkit
- Add more ISOs anytime by copying them to the drive.
- Organize by folders for clarity.
- Test new additions before relying on them in production.


# 🧭 Easy2Boot Best Practices & Quick Start Guide

## 📂 Best Practices

### Organization
- Use the **predefined Easy2Boot folder hierarchy** (`\_ISO\WINDOWS`, `\_ISO\LINUX`, `\_ISO\UTILITIES`, etc.) to ensure ISOs appear correctly in the boot menu.
- Apply **clear, descriptive file names** (e.g., `Win11_Pro_x64.iso`, `Ubuntu_24.04.iso`) since filenames are displayed in the boot menu.
- For large collections, consider **optional subfolders** (e.g., `/Windows/Legacy` vs `/Windows/UEFI`) to keep your toolkit structured, while still respecting Easy2Boot’s detection rules.

### Testing
- Always **test new ISOs** in both BIOS and UEFI modes before field use.
- Verify installers and utilities boot correctly across different hardware types.

### Maintenance
- Keep Easy2Boot updated with the **latest version**.
- Remove outdated ISOs to save space and avoid confusion.
- Regularly check drive health if using a portable SSD/HDD.

### Compatibility
- **Disable Secure Boot** in UEFI/BIOS settings.
- Document any ISOs that require special configuration for future reference.

### Reliability
- Maintain a **backup copy** of your Easy2Boot drive.
- Carry a small secondary USB stick with a single “emergency” ISO (e.g., WinPE or Hiren’s BootCD) as a fallback.
