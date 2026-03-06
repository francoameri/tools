🔧 Integration with PowerShell
Ninite installers are **single executables** that already contain the list of apps you selected on the website. PowerShell doesn’t let you “choose apps on the fly” — you must **pre‑select the apps on ninite.com**, download the custom installer, and then call it from PowerShell.

```plaintext
# Run Ninite installer silently with PowerShell
Start-Process -FilePath "C:\Installers\Ninite.exe" -ArgumentList "/silent" -Wait
```

- /silent ensures no UI interaction.
- Running as Administrator installs system‑wide.
- **You can schedule this script with Task Scheduler or Intune for automation.**
- Replace "C:\Installers\Ninite.exe" with the path where you have placed Ninite's installer.

📦 Disclaimer - Selecting Apps
- **You cannot** select all apps dynamically from PowerShell.
- The selection happens beforehand on the Ninite website (you tick the apps you want).
- The downloaded installer is tied to that selection — every time you run it, it installs/updates those same apps.

🔄 Updating Apps
The beauty of Ninite is that the same installer can be reused:
- Run it again later → it **updates all chosen apps to their latest versions.**
- No need to re‑download unless you want to change the app list.

## 📥 Downloadable Script
For practical integration, a ready‑to‑use PowerShell script is included in this repository.  
You can download it here:  

[Ninite-Installer-Script](ninite-install.ps1)

This script demonstrates how to run the Ninite installer silently with PowerShell, making it easy to automate deployments or updates across multiple systems.


> ⚠️ **Note:** Place your downloaded `Ninite.exe` in the correct path referenced in the script before execution or edit it's path with notepad or any text-processing software.


⏰ Automating with Task Scheduler from Windows
You can **configure Windows Task Scheduler to run the ninite-install.ps1 script on a regular basis**, ensuring your selected applications stay updated automatically.
Steps:
- Open Task Scheduler (taskschd.msc from Run - Start+R - or Start Menu).
- Click Create Basic Task.
- Give it a name (e.g., Ninite Weekly Update).
- Choose Weekly as the trigger and set the desired day/time.
- For the Action, select Start a Program.
- In the Program/script field, enter:

```plaintext
powershell.exe
```

- In the Add arguments field, specify the path to your script:

```plaintext
- ExecutionPolicy Bypass -File "C:\Path\To\ninite-install.ps1"
```

- Finish the wizard and ensure the task runs with highest privileges (check the box in task properties).
Benefits:
**- Keeps apps updated without manual intervention.**
**- Ensures consistency across systems.**
**- Works seamlessly with the reusable Ninite installer.**
