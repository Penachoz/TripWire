# 🕵️ Tripwire – Real-Time File System Watcher

**Tripwire** is a lightweight, Python-based digital forensics tool built to detect and capture **suspicious temporary file activity in real-time**. It's especially useful in **dynamic malware analysis**, sandbox testing, and detecting **fileless or evasive threats** that drop payloads briefly during execution.

> 🔍 Designed for **threat hunters**, **blue teams**, and **infosec students** learning malware behavior and live system monitoring.

---

## 🚀 Features

- 📂 **Monitors multiple directories** simultaneously.
- 🧠 **Extension filtering** — only track file types of interest.
- 🕒 **Real-time detection** with 0.1s scan interval.
- 🚫 **Exclude** specific extensions or folders to reduce noise.
- 📸 **Auto-snapshots** suspicious file drops with timestamped logs.
- 🎨 Colored CLI interface using `colorama` for visibility.

---

## 🖥️ Demo

![Tripwire in action](https://github.com/user-attachments/assets/265b1abd-49c2-4613-95af-aa5df3883e17)

---

## ⚙️ Installation & Usage

### 🔧 Clone and Run via Python (Cross-platform)
```bash
git clone https://github.com/yourusername/Tripwire.git
cd Tripwire
pip install -r requirements.txt
python Tripwire.py
```

### 💻 Windows Executable (Faster Startup)
```bash
.\Tripwire.exe
```

> You can compile your own executable using `pyinstaller`:
```bash
pyinstaller --onefile Tripwire.py
```

---

## 🛠️ Configuration

Edit the `Tripwire.py` file to configure:

```python
WATCH_PATHS = ["C:\\Users\\user\\AppData\\Local\\Temp", "/tmp"]
EXTENSIONS = [".exe", ".dll", ".bat", ".ps1"]
EXCLUDE = [".log", ".tmp"]
```

- `WATCH_PATHS`: List of folders to monitor.
- `EXTENSIONS`: File types to flag.
- `EXCLUDE`: Optional exclusions to reduce false positives.

---

## 📚 Use Cases

- Malware sandbox monitoring.
- Detecting suspicious behavior from document macros or PowerShell scripts.
- Lab environment surveillance (e.g. HTB, TryHackMe, malware samples).
- Forensics training and CTF automation.

---

## ✅ Requirements

- Python 3.7+
- `watchdog`  
- `colorama`

Install with:
```bash
pip install watchdog colorama
```

---

## 📄 License

MIT License. Built for educational and research purposes.

---

## 👨‍💻 Author

David Penagos  
💼 Aspiring SOC Analyst | Cybersecurity Enthusiast  
🔗 [LinkedIn](https://www.linkedin.com/in/david-penagos-b30406246)  
🔗 [GitHub](https://github.com/Penachozz)
