# ⚠️ Bash Script Exit Codes & Error Handling — Complete Guide (2026)

![Linux](https://img.shields.io/badge/Linux-Guide-blue)
![Level](https://img.shields.io/badge/Level-Intermediate%20to%20Advanced-green)
![Updated](https://img.shields.io/badge/Updated-2026-orange)
![Focus](https://img.shields.io/badge/Focus-Error%20Handling-important)

> Your script ran… but silently failed?  
> Understanding exit codes and error handling is the difference between fragile scripts and reliable automation.

📖 **[Full Guide (exit codes + traps + best practices → linuxteck.com)](https://www.linuxteck.com/bash-script-exit-codes-and-error-handling/?utm_source=github&utm_medium=repo&utm_campaign=exit-codes)**

---

## ⚡ 1-Minute Understanding

If you remember just this:

- `0` → success  
- Non-zero → error  
- `$?` → last command status  

💡 Every script should handle errors explicitly.

---

## 🖼️ Preview

> Checking exit status in Bash scripts

![Preview](https://raw.githubusercontent.com/linuxteck/bash-exit-codes/main/exit-preview.png)

---

## 🧠 Why This Guide Exists

Many scripts fail silently — causing bigger problems later.  
Proper error handling makes scripts predictable and safe.

This guide helps you:
- Understand exit codes clearly  
- Handle errors properly  
- Build production-ready scripts  

---

## 🔄 Common Exit Codes

| Code | Meaning |
|------|--------|
| `0` | Success |
| `1` | General error |
| `2` | Misuse of command |
| `126` | Permission denied |
| `127` | Command not found |
| `130` | Script terminated (Ctrl+C) |

---

## 👉 Want full examples, traps, and advanced handling?  
Read here:  
https://www.linuxteck.com/bash-script-exit-codes-and-error-handling/?utm_source=github&utm_medium=repo

---

## 🚀 Basic Usage (Copy-Paste Ready)

```bash
# Run a command
ls file.txt

# Check exit code
echo $?
```

---

## 🧪 Simple Error Handling

```bash
#!/bin/bash

if [ $? -ne 0 ]; then
  echo "Error occurred"
fi
```

---

## 🧪 Best Practices

```bash
# Exit on error
set -e

# Print commands (debugging)
set -x

# Handle errors manually
if ! command; then
  echo "Command failed"
  exit 1
fi
```

---

## 🎯 When Should You Use This?

```bash
# Automation scripts
# Deployment pipelines
# Backup scripts
# Production systems
```

---

## 🎯 Who Gets the Most Value

| You Are | Benefit |
|---------|--------|
| 🟢 Beginner | Understand script behavior |
| 🔵 Sysadmin | Build reliable scripts |
| 🔴 DevOps Engineer | Prevent silent failures |
| 🟡 Developer | Debug scripts efficiently |

---

## 🔗 More LinuxTeck Guides You'll Want

> 📂 *Part of the **LinuxTeck Master Series** — practical Linux guides*

- ⚡ https://www.linuxteck.com/modern-linux-tools/
- 📊 https://www.linuxteck.com/linux-logging-best-practices/
- 🔐 https://www.linuxteck.com/uefi-secure-boot-linux/
- 🔤 https://www.linuxteck.com/sort-command-in-linux/
- 🔍 https://github.com/linuxteck?tab=repositories

---

## ✍️ About LinuxTeck

**https://www.linuxteck.com** publishes practical, real-world Linux guides — no fluff, no filler.  
If you write scripts, these guides will save you from costly mistakes.

⭐ Found this useful? Star this repo — it helps more developers write better scripts  
🔁 Share with your team — especially if scripts fail silently 😄  
👤 https://github.com/linuxteck

---

**Topics:** bash • linux • exit-codes • error-handling • shell-scripting • devops • sysadmin • automation • debugging • scripting
