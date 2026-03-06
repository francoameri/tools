## ⏰ Automating with Task Scheduler from Windows
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
  
📌 **Benefits:**

- Keeps apps updated without manual intervention.
- Ensures consistency across systems.
- Works seamlessly with the reusable Ninite installer.


---

## 🌐 Network Deployment with Ninite

Want to do this in a bigger scale? Check this other document:

![Network-Deployment](./network-deployment/readme.md)
