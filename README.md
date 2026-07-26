AI was used to make this app. All the ideas were my own, and it took time to get it right. It was a personal project born from some issues I have with Docker. I do not like using PowerShell or CMD, and this fixes that without ever touching the CMD. It also fixes an issue where if a drive was unplugged, you can re-run the setup to re-mount that drive. Furthermore, if it is already set up, the setup will never touch your existing settings; it will only apply any new changes you have made. 


# 📋 Master Installation & Configuration Guide

---

### Step 1️⃣: Prowlarr Setup
> *Use your own set ports if you changed them.*

#### 1. Radarr Integration
* **Radarr:** Go to `http://localhost:7879/` → **Settings** → **General** → Copy **API key**
* **Prowlarr:** Go to `http://localhost:9697/` → **Settings** → **Apps** → **Applications** → **`+`** → **Radarr**
* **Prowlarr Server:** Change to `http://prowlarr:9696`
* **Radarr Server:** Change to `http://radarr:7878`
* Paste your API key and save.

---

### Step 2️⃣: Sonarr Integration
> *Use your own set ports if you changed them.*

* **Sonarr:** Go to `http://localhost:8990/` → **Settings** → **General** → Copy **API key**
* **Prowlarr:** Go to `http://localhost:9697/` → **Settings** → **Apps** → **Applications** → **`+`** → **Sonarr**
* **Prowlarr Server:** Change to `http://prowlarr:9696`
* **Sonarr Server:** Change to `http://sonarr:8989`
* Paste your API key and save.

---

### Step 3️⃣: Lidarr Integration
> *Use your own set ports if you changed them.*

* **Lidarr:** Go to `http://localhost:8686/` → **Settings** → **General** → Copy **API key**
* **Prowlarr:** Go to `http://localhost:9697/` → **Settings** → **Apps** → **Applications** → **`+`** → **Lidarr**
* **Prowlarr Server:** Change to `http://prowlarr:9696`
* **Lidarr Server:** Change to `http://lidarr:8686`
* Paste your API key and save.

---

### Step 4️⃣: qBittorrent Connection
> *You will need your Username and Password for this section. Use your set ports if changed.*

* **Prowlarr:** Go to **Settings** → **Download Clients** → **`+`** → **qBittorrent**
* **Host:** `qBittorrent`
* **Port:** Your set port (Default is `8080`)
* **Username:** `[Your qBittorrent Username]`
* **Password:** `[Your qBittorrent Password]`
* Click **Test & Save**.
* *Note:* If you run into an **Authentication failure**, turn the stack off and on, then try again.

---

### 📂 Recommended Media Folder Structure

```text
Media
├── Anime
├── Movies
├── Music
├── TV
└── Downloads
    ├── incomplete
    └── completed

```
Option A: Using Separate Incomplete/Completed Folders
If you follow the folder structure above, configure qBittorrent with these save paths:

Default Save Path: /data/media/Downloads/completed

Keep incomplete in: /data/media/Downloads/incomplete

Option B: Using a Single Folder
If you don't want a separate incomplete folder, leave it turned off and point everything to the main downloads folder:

Default Save Path: /data/media/Downloads

⚠️ Additional Troubleshooting & Tips
If you run into any issues, try the following steps:

🔄 Refresh / Restart Stack: No settings will be lost. Just turn the stack off and on again 😆.

☢️ NUKE IT: Uninstall the system stack and start over 😆.

---

🐛 Bug Tracker
Minor known bugs that are not critical issues:

The UI allows selecting a file and pressing the confirm button even if no Docker-Compose file is present in that directory, and it will still incorrectly report success.

---

Anyway here is some pretty pictures so you know what it looks like. Enjoy!

---

<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-41-44" src="https://github.com/user-attachments/assets/0331dfcf-7702-4976-8d65-40f5d7bfe450" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-44-00" src="https://github.com/user-attachments/assets/97667824-9096-4141-9a17-9a0223b8ae8a" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-44-26" src="https://github.com/user-attachments/assets/1b9fc4a7-11f3-4dfe-8755-c6dcc8179924" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-44-27" src="https://github.com/user-attachments/assets/0484bed9-cd3d-4d05-b641-a438dfe5de55" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-44-44" src="https://github.com/user-attachments/assets/a04ee970-d4b4-4495-af1a-79b3b1720b98" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-44-53" src="https://github.com/user-attachments/assets/ab0cdc95-ba23-4653-bcec-f5e51a918980" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-44-56" src="https://github.com/user-attachments/assets/1d1a1225-0559-4d29-95e7-11f47fe82ce7" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-45-11" src="https://github.com/user-attachments/assets/8e3f421a-74fc-481c-aa49-f31bf9c64a16" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-45-18" src="https://github.com/user-attachments/assets/12e9c559-306e-4339-89ff-1a6c7df618b9" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-45-23" src="https://github.com/user-attachments/assets/96883e63-89ae-4b20-b1c8-024389e5f7ae" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-45-39" src="https://github.com/user-attachments/assets/f709b250-6646-4a89-8f9b-96fb872900e6" />
<img width="1307" height="1057" alt="Screenshot 2026-07-25 06-47-16" src="https://github.com/user-attachments/assets/4760b4b0-5369-46dd-8f5c-8f5ac905c1c3" />

---
