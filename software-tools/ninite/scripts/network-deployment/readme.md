🌐 Network Deployment with Ninite
This guide explains how to run Ninite from a shared network folder and automate updates across multiple endpoints in a small business environment.

📂 Centralized Script Setup
- Create a shared folder on a server that every endpoint with Windows that you want to automate updates with Ninite, e.g.:

```plaintext
\\Server\IT\Ninite\
```

- Place the following files inside:
  
```plaintext
- Ninite.exe → your custom installer with selected apps.
- ninite-install.ps1 → PowerShell script to run Ninite silently.
```

⏰ Automating with Task Scheduler
You can configure each endpoint to run the script weekly

> See this step in [!Integration-with-Powershell](..scripts/readme.md)

📌 Export/Import for Replication
To replicate across multiple endpoints:

```plaintext
- Configure the task once.
- Right‑click → Export → save as .xml.
- On other machines → Import Task… → adjust script path if needed.
```

> This is faster for environments with standardized paths.

🏢 Group Policy Deployment (Domain Environments)
If your endpoints are domain‑joined:

```plaintext
- Use Group Policy Preferences → Scheduled Tasks.
- Push the task to all machines at once.
- Ensure the UNC path is accessible to all endpoints.
```

This method provides centralized control and reduces manual effort

---

🎯 Best Practices
- Centralize scripts → update once, all endpoints benefit.
- Run as SYSTEM or service account → ensures installs succeed without user login.
- Test on one machine first → confirm permissions and paths.
- Document schedule → align with maintenance windows to avoid disruption.
