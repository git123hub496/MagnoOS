# MagnoOS

**MagnoOS** is a lightweight, fast, and straightforward operating system based on Linux Mint. We stripped out the bloat to give you a clean desktop that uses less RAM and stays easy to use.

---

## Why MagnoOS?

MagnoOS is built around **security**, **stability**, **flexibility**, and **customization**—giving you full control over your desktop without unnecessary background services slowing you down.

### Built-In Magno Features
* **Magno Clipboard:** Keeps a searchable history of everything you copy.
* **Magno Screenshots:** A fast, simple, and easy-to-use screenshot tool.
* **Magno Spotlight:** Search the web and your local files from one place.
* **Magno Mirror:** Mirror and interact with your phone screen right from your desktop *(Android only)*.
* **Magno Updater:** Delivers system updates at least once a week.

---

## System Requirements
* **CPU Architecture:** AMD64 / x86_64 *(Only AMD processors are supported at the moment)*
* **USB Flash Drive:** 8 GB or larger

---

## Step 1: Download & Reassemble the ISO

Because GitHub limits individual release files to 2 GB, the 6 GB MagnoOS ISO is split into four parts. Download **all four parts** (`MagnoOS.iso.part00` through `MagnoOS.iso.part03`) from the [Releases](../../releases) page into the same folder, then reassemble them using the command for your current OS:

### Linux / macOS
```bash
cat MagnoOS.iso.part* > MagnoOS.iso
```

### Windows (Command Prompt)
```cmd
copy /b MagnoOS.iso.part* MagnoOS.iso
```

### Verify Your Download (Optional)
Run a SHA-256 check to make sure your reassembled ISO is complete and uncorrupted:
* **Linux:** `sha256sum MagnoOS.iso`
* **macOS:** `shasum -a 256 MagnoOS.iso`
* **Windows (Command Prompt):** `certutil -hashfile MagnoOS.iso SHA256`

Expected SHA-256 checksum:
```text
<c4cde40b042dafbe229a2e8505572aa7ba29f329fe2bb1bd1b943228888e9226>
```

---

## Step 2: Flash & Boot MagnoOS

1. Download and open [balenaEtcher](https://balena.io).
2. Select your reassembled `MagnoOS.iso` file and your USB flash drive (**8 GB or larger**), then click **Flash**.
3. Restart your PC and open your **One-Time Boot Menu** (commonly `F12`, `F11`, `F2`, or `Esc` depending on your motherboard).
4. Select your USB drive and follow the **First-Boot Menu** steps on screen to set up MagnoOS.

---

## Step 3: Install to Your Internal Drive

Once you finish the first-boot setup, MagnoOS will still be running live from your USB flash drive. To install it permanently onto your internal SSD or hard drive:

1. Open the terminal and run:
   ```bash
   sudo magno-install-ssd
   ```
2. Enter your `sudo` password when prompted.
3. Restart your computer once the installer tells you it is finished (and remove your USB drive). MagnoOS will now boot directly from your computer!

---

## Step 4: Installing Updates

After booting into your installed system, check for the latest updates:

1. Open the **Magno Grid** by pressing the **Super** (Windows) key and open **Magno Updater**.
2. Click the **Check_Install Updates** button and wait for the updates to finish installing.
3. Restart your computer when prompted to apply your MagnoOS updates.
