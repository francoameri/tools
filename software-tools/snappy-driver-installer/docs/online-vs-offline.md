# Snappy Driver Installer (SDI) – Online vs Offline Usage

📌 Snappy Driver Installer (SDI) can be used in two distinct modes: **Online (Lite)** and **Offline (Full Driver Pack)**.  
Each mode has advantages and trade-offs depending on your environment, infrastructure, and workflow.

---

## 🌐 Online Mode (Lite Version)
- **How it works:** SDI downloads drivers on demand directly from the internet.
- **Pros:**
  - Lightweight download (~5 MB).
  - Portable — can run from a USB stick without installation.
  - Always fetches the latest drivers available.
  - Saves disk space (no need to store 50+ GB locally).
- **Cons:**
  - Requires a stable internet connection.
  - Slower in environments with limited bandwidth.
  - Not ideal for large-scale or repeated deployments.

**Best for:**  
Casual fixes, single endpoint troubleshooting, or environments with reliable internet access.

---

## 💾 Offline Mode (Full Driver Pack)
- **How it works:** SDI uses a locally stored driver repository (~50+ GB).
- **Pros:**
  - Works completely offline — no internet required.
  - Faster deployments across multiple endpoints.
  - Ideal for technicians working in restricted or secure environments.
  - Ensures consistent driver availability across sites.
- **Cons:**
  - Large initial download (50+ GB).
  - Requires regular updates to keep driver packs current.
  - Needs significant storage space.

**Best for:**  
IT technicians, infrastructure deployments, server environments, or scenarios where **internet access is limited or restricted.**

⚠️ **Personal recommendation:**
It's really useful to have this tool **BOTH** in Offline Mode inside a USB Stick - with enough space - and in an accesible network drive.
- In a USB stick, for cases when you don't have access to the network - sometimes you find a deploy doesn't have network drivers.
- In a network drive, because sometimes you are working remotely and you don't have access to the physical device.

---

## ⚖️ Choosing the Right Mode
- **Online Lite** → Quick fixes, portable troubleshooting, minimal storage.  
- **Offline Full Pack** → Enterprise-scale deployments, secure networks, repeated use across endpoints and servers.
