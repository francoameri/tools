# How to Use Snappy Driver Installer (SDI)

Snappy Driver Installer (SDI) can be used in two modes: **Online (Lite)** and **Offline (Full Driver Pack)**.  
This guide explains how to set up and use both approaches safely and effectively.

---

## 🌐 Online Mode (Lite Version)

### 📥 Download
- Get the **Lite version** from the official site: [SDI Lite Download](https://sdi-tool.org/download/).

### ▶️ Steps
1. **Extract the archive** to a folder, USB drive or network folder.
2. **Run `SDI_x64.exe` or `SDI_x86.exe`** depending on your system.
3. SDI will **scan your hardware** and list missing or outdated drivers.
4. Select the drivers you want to install.
5. SDI will **download drivers on demand** from the internet.
6. A **system restore point** is created automatically before installation - you will have to click on the checkbox!.
7. Drivers are installed, and you can reboot if required.

```
+---------+       +-----------+       +------------+       +-------------------+       +----------------+
|  Launch | --->  |   Scan    | --->  |  Download  | --->  | Restore Point Made| --->  | Install Driver |
+---------+       +-----------+       +------------+       +-------------------+       +----------------+
```

### ✅ Best For
- Quick fixes on single endpoints.
- Portable troubleshooting with minimal storage.
- Environments with reliable internet access.

---

## 💾 Offline Mode (Full Driver Pack)

### 📥 Download
- Get the **Full version** (with driver packs, ~50GB) from the official site: [SDI Full Download](https://sdi-tool.org/download/).

### ▶️ Steps
1. **Download and extract** the full driver pack to a local folder or external drive.
2. **Run `SDI_x64.exe` or `SDI_x86.exe`**.
3. SDI will **scan your hardware** and match drivers against the local repository.
4. Select the drivers you want to install.
5. A **system restore point** is created automatically before installation - you will have to click on the checkbox!.
6. Drivers are installed instantly from the local pack — no internet required.
7. Reboot if necessary.

```
+---------+       +-----------+       +----------------+       +-------------------+       +----------------+
|  Launch | --->  |   Scan    | --->  | Local Driver DB| --->  | Restore Point Made| --->  | Install Driver |
+---------+       +-----------+       +----------------+       +-------------------+       +----------------+
```

### ✅ Best For
- Large-scale deployments across multiple endpoints.
- Secure or restricted environments without internet access.
- Faster repeated installations in enterprise or server scenarios.

---

## 🔒 Security Notes
- SDI **automatically creates a system restore point** before changes, so long as you click on the checkbox.
- No adware, bloatware, or hidden installs — it’s clean and open source.
- Always download from the official site: [https://sdi-tool.org/](https://sdi-tool.org/).

---

## ⚡ My Experience
I am **not the owner or developer** of SDI — I am an advanced user who has relied on it extensively in infrastructure deployments across endpoints and servers.  
Both modes have saved me countless hours compared to manual driver hunting, and the restore point feature has provided peace of mind in production environments.
