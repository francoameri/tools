# ⚡ Easy2Boot Setup & Quickstart Guide

## 1️⃣ Download Easy2Boot
- Download **[Easy2Boot](https://easy2boot-xyz.translate.goog/download/)** as a self‑extracting `.exe` (recommended).  
- After running the `.exe`, a new folder will be created on your **Desktop** containing the install files.  
- ⚠️ You may need to ignore the Windows Defender SmartScreen warning and choose **Run anyway**.  

---

## 2️⃣ Make a USB Drive (Win10/11 Recommended)
- Run **Make_E2B.exe** to create your Easy2Boot USB drive.  
- You can use either a **USB Flash drive** or a **USB hard disk/SSD**.  
- ⚠️ All partitions and contents on the USB drive will be erased.  

**Steps:**
1. Select E2B menu options.  
2. Select the USB drive (if a drive letter is visible).  
3. Click the **Big Red Arrow** button.  
   - Use the **Gear Wheel** button if you want special options (e.g., multiple partitions, custom sizes, or if no drive letter is listed).  

**Additional Options:**
- Type **Y** to install **agFM** (direct UEFI booting).  
- Type **Y** to install **Ventoy for Easy2Boot** (alternative menu system).  

**Notes:**
- To add UEFI agFM files to the second partition, you need **Windows 10/11** if your USB drive is a *Removable Flash drive*.  
- If your USB drive is a *Fixed Disk type* (HDD/SSD or certain flash drives), you can use XP/Win7/Win8/Win10 without restrictions.  
- Only recent (2021+) Windows 10 builds allow access to multiple partitions on removable USB flash drives.  

**Troubleshooting:**
- If the script fails, run:

```
_ISO\docs\Make_E2B_USB\Drive\DebugAll_MakeE2B_Admin.cmd
```

as Administrator, then check `e2b.log`.  
- Disable antivirus temporarily if issues occur.  
- Developer versions of Win10/11 do not include `wmic.exe` — use a full retail or volume licensed version of Windows.  

---

## 3️⃣ Add Payload Files (ISO, WIM, EFI, VHD, etc.)
### 3.1 Copy Files
- Copy bootable files into the **predefined menu folders** on the first partition:  

```
_ISO\MAINMENU
_ISO\ANTIVIRUS
_ISO\BACKUP
_ISO\DOS
_ISO\LINUX
_ISO\UTILITIES _ISO\UTILITIES_MEMTEST
_ISO\WIN (WindowsToGo VHD/VHDx files)
_ISO\WINPE (HBCD_PE, Strelec, DLCBoot, Gandalf)
_ISO\WINDOWS\xx (Windows Install ISOs and images)
```

- Example:  
- Copy a Windows 10 ISO into `\_ISO\WINDOWS\WIN10`.  
- Copy a Linux ISO into `\_ISO\LINUX` or `\_ISO\MAINMENU`.  

- You can create **new sub‑menu folders** by running the provided Windows batch file.

### 3.2 Make Files Contiguous
- After copying payload files, run:  

```
\MAKE_THIS_DRIVE_CONTIGUOUS.cmd
```

on the USB drive.  
- This ensures all payload files are contiguous (required for some operations, though not for Windows ISOs).  
- Run this again whenever new payload files are added.  

---

You now have a **multiboot USB drive** ready for BIOS and UEFI environments (Secure Boot disabled).

> Important note: Installing E2B can be quite complex, so here's the full guide and a video from the author's website in case you need it:

[E2B Install Guide](https://easy2boot.xyz/download/)

[![E2B Install Process](https://img.youtube.com/vi/J7XjH-eLjbg/0.jpg)](https://www.youtube.com/watch?v=J7XjH-eLjbg)

---

# 📝 Easy2Boot Quick Reference Cheat Sheet

## 🔧 Setup
1. Download Easy2Boot (`.exe` for Win7/8/10/11, `.zip` for XP).
2. Run **Make_E2B.exe** → select USB drive → click **Big Red Arrow**.
   - Use **Gear Wheel** for custom partitions.
   - Type `Y` to install agFM (UEFI boot).
   - Type `Y` to install Ventoy for Easy2Boot (optional).

## 📂 Payload Files
Copy bootable files into predefined folders:

```
_ISO\MAINMENU
_ISO\ANTIVIRUS
_ISO\BACKUP
_ISO\DOS
_ISO\LINUX
_ISO\UTILITIES
_ISO\UTILITIES_MEMTEST
_ISO\WIN (WindowsToGo VHD/VHDx files)
_ISO\WINPE (HBCD_PE, Strelec, DLCBoot, Gandalf)
_ISO\WINDOWS\xx (Windows Install ISOs and images)
```

## 📏 Contiguous Files
Run on USB drive after adding ISOs:

```
\MAKE_THIS_DRIVE_CONTIGUOUS.cmd
```

## 📝 Notes
- Disable **Secure Boot** in UEFI/BIOS.
- Windows 10/11 required for UEFI files on removable flash drives.
- Use retail/volume licensed Windows (not developer builds).
- Backup your Easy2Boot drive regularly.
- - 🛠️ Quick Troubleshooting: Run `DebugAll_MakeE2B_Admin.cmd` as Administrator if setup fails.

---

## ✅ Summary
- **Step 1**: Download Easy2Boot.  
- **Step 2**: Use `Make_E2B.exe` to prepare your USB drive.  
- **Step 3**: Copy ISOs/WIMs/VHDs into the correct `\_ISO` folders.  
- **Step 4**: Run `MAKE_THIS_DRIVE_CONTIGUOUS.cmd` to finalize.  
