# 🛡️ Aegis Automated Perimeter Security Dashboard

```text
  [ Smartphone Camera / Test Stream ]
                 │
                 ▼
     [ FastAPI Security Server ] ────► Logs saved to: security_breaches.log
     (Runs inside VirtualBox VM)
                 │
                 ▼
   [ Windows PC Desktop Browser ] ───► View live at: http://127.0.0.1:8000
```

This project is a lightweight, high-speed automated security monitoring system. It processes a video stream, automatically tracks moving targets, flashes alerts when a boundary line is crossed, and saves security logs straight to the computer's hard drive.

---

## ✨ System Features

* **Real-Time Target Tracking:** Tracks moving objects across the screen cleanly without lagging or crashing the system.
* **Instant Safety Alerts:** Flashes a visual warning screen the exact second an object crosses the red boundary tripwire line.
* **Automatic Security Logging:** Writes a permanent, timestamped record of every security breach directly into a text log file (`security_breaches.log`).
* **Web Control Panel:** Includes a clean web page dashboard so security operators can monitor the live camera stream and system statistics side-by-side.

---

## 🛠️ Tech Stack

* **Programming Language:** Python 3.12
* **Web Server Framework:** FastAPI & Uvicorn
* **Computer Vision:** OpenCV & NumPy
* **Deployment Environment:** VirtualBox (Linux Engine Node)

---

## 🚀 How to Run the Project Local Workspace

Follow these simple terminal commands to start the security platform.

### 1. Open the project folder
```bash
cd ~/aegis-env-security
```

### 2. Turn on the server
```bash
/home/maths/.local/bin/uvicorn src.main:app --host 10.0.2.15 --port 8000
```

### 3. Open the live dashboard
Open the web browser on your computer desktop and type in this address:
```text
http://127.0.0.1:8000
```

### 4. Watch the live security logs
To watch your computer write security breach timestamps in real time, open a second terminal and run:
```bash
tail -f ~/aegis-env-security/security_breaches.log
```
