
````markdown
# Install Ubuntu 24.04 on Android Without Root

This guide explains how to install **Ubuntu 24.04 LTS** on an Android device **without rooting**, using **Termux** and a container-based Linux environment.

> ⚠️ Important  
> Install **Termux only from F-Droid or GitHub**.  
> The Play Store version is outdated and may cause errors.

---

## 📌 Requirements

Before starting, ensure you have:

- Android device (Android 7.0 or higher)
- Minimum **3 GB RAM** recommended (4 GB+ preferred)
- At least **8–10 GB free storage**
- Stable internet connection

---

## 📲 Required Apps (APK Download Links)

### 1️⃣ Termux (Mandatory)

Install **Termux** from **one of the official sources below**:

- 🔹 **F-Droid (Recommended):**  
  https://f-droid.org/packages/com.termux/

- 🔹 **GitHub Releases:**  
  https://github.com/termux/termux-app/releases

❌ Do **NOT** install Termux from the Play Store.

---

### 2️⃣ VNC Viewer (For Desktop GUI)

Install **VNC Viewer** from Play Store:

- 🔹 **Google Play Store:**  
  https://play.google.com/store/apps/details?id=com.realvnc.viewer.android

---

## 🚀 Installation Steps

### 1️⃣ Update Termux Packages

```bash
apt update && apt upgrade -y
````

---

### 2️⃣ Install Required Tools

```bash
pkg install wget git -y
```

---

### 3️⃣ Download Ubuntu Setup Script

```bash
wget https://raw.githubusercontent.com/modded-ubuntu/modded-ubuntu/refs/heads/master/setup.sh
```

---

### 4️⃣ Give Execute Permission

```bash
chmod +x setup.sh
```

---

### 5️⃣ Run the Installer

```bash
./setup.sh
```

* Type **`y`** when prompted
* Allow **storage permission** if requested
* Installation may take several minutes

---

### 6️⃣ Restart Termux

Close Termux completely and reopen it.

---

### 7️⃣ Start Ubuntu

```bash
ubuntu
```

---

### 8️⃣ Create Ubuntu User

```bash
bash user.sh
```

* Enter a **lowercase username**
* No spaces allowed

---

### 9️⃣ Restart Termux Again

Close and reopen Termux.

---

### 🔟 Launch Ubuntu

```bash
ubuntu
```

---

## 🖥️ Install Ubuntu Desktop (GUI)

To install a graphical desktop environment:

```bash
sudo bash gui.sh
```

* Create a **VNC password**
* Remember this password for VNC login

---

## 🖱️ Access Ubuntu Desktop via VNC

1. Open Termux and start Ubuntu:

   ```bash
   ubuntu
   ```

2. Start VNC server:

   ```bash
   vncstart
   ```

3. Open **VNC Viewer**

4. Create a new connection:

   * **Address:** `localhost:1`
   * **Name:** `Ubuntu 24.04`

5. Connect and enter your VNC password

🎉 Ubuntu desktop will appear.

---

## 🛠️ Useful Commands

| Task            | Command                                  |
| --------------- | ---------------------------------------- |
| Enter Ubuntu    | `ubuntu`                                 |
| Start VNC       | `vncstart`                               |
| Stop VNC        | `vncstop`                                |
| Update Ubuntu   | `sudo apt update && sudo apt upgrade -y` |
| Install package | `sudo apt install <package-name>`        |

---

## 🗑️ Uninstall Ubuntu

To completely remove Ubuntu:

```bash
bash remove.sh
```

---

## ❓ Notes

* No root access required
* Runs in a safe container environment
* Performance depends on device hardware
* Best experience on **4 GB+ RAM** devices

---

## ⚡ One-Command Full Setup (Automatic)

Run this **single command** in **Termux** to install Ubuntu 24.04:

```bash
apt update && apt upgrade -y && pkg install wget git -y && wget https://raw.githubusercontent.com/modded-ubuntu/modded-ubuntu/refs/heads/master/setup.sh && chmod +x setup.sh && ./setup.sh
```

### After Installation

```bash
ubuntu
bash user.sh
sudo bash gui.sh
vncstart
```

✅ Ubuntu 24.04 with full desktop is now ready.

---

## ✅ Conclusion

You now have **Ubuntu 24.04 LTS running on Android without root**, including a complete desktop GUI using VNC.

Perfect for:

* Linux learning
* Development & coding
* Testing software on mobile

Happy Linuxing 🐧🚀

```
