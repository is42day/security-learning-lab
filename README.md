# 🧪 Security Learning Lab

This is a hands-on local lab for learning and testing real-world security exploits, CVEs, and enumeration techniques using Docker + VS Code + DevContainers.

---

## 📦 What’s Inside

### ✅ Lab Environment
- Docker-based targets using [Vulhub](https://github.com/vulhub/vulhub)
- Local devcontainer for running tools (nmap, wpscan, curl, etc.)
- Clean separation of lab targets and tools
- Designed to run **offline** after setup

### ✅ Current Setup
| Target | CVE / Exploit | Status |
|--------|---------------|--------|
| WordPress (Pwnscriptum) | RCE via vulnerable plugin (wp-file-manager) | ✅ Complete |
| Redis | CVE-2022-0543 (abandoned) | ❌ Dropped |

---

## 🚀 How to Use

### 🧱 Build the Lab
```bash
cd targets/vulhub/wordpress/pwnscriptum
docker-compose up -d

🛠 Dev Tools (from devcontainer)
bash
Copy
Edit
nmap -Pn -sV ...
wpscan --url http://host.docker.internal:8088
curl -X POST -F "upload[]=@shell.php" ...

✅ Status
🔒 Runs entirely locally

📁 All Docker-based labs isolated by folder

📚 Learning-focused, well-documented

🔧 Uses DevContainers + VS Code

📎 Notes
This project is for educational and research purposes only.
Do not expose any containers to the public internet.
Always get authorization before testing on any non-owned system.

🔗 Credits
Vulhub

Exploit-DB

WPScan

You

