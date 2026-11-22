# GCRE — Kibana ELK 8 SOC Automation

A lightweight Chrome extension built for SOC analysts to automate repetitive triage and rule-management tasks in **Kibana (ELK 8.x)**. Works dynamically on any ELK 8 instance and Kibana Space using your active browser session—no API keys or hardcoded IPs required.

---

## ⚡ Features

* **Notes & Triage:** Auto-scrolls the alerts table, extracts all `kibana.alert.uuid` values, and bulk-applies notes (with built-in RTL/mixed-language formatting), `False Positive` tags, and alert closing.
* **Bulk Note Cleaner (`DEL NOTES`):** Scans visible alerts, fetches attached notes, and deletes them in one click.
* **SIEM Rule Auto-Importer (`RULE IMPORT`):** Injects a floating HUD on Kibana to sequentially import folders of `.ndjson` detection rules with a configurable delay (default: `3s`) and overwrite options.
* **Space-Aware & Live Terminal:** Automatically detects your current Kibana Space (`/s/...` or `default`) and displays real-time execution logs.

---

## 🚀 Installation (Chrome)

1. Download or clone this repository and extract the `GCRE` folder.
2. Open Chrome and navigate to `chrome://extensions`.
3. Enable **Developer mode** (top-right corner).
4. Click **Load unpacked** and select the extracted extension folder (the one containing `manifest.json`).
5. *(Optional)* Click the puzzle icon in the Chrome toolbar and **Pin** **GCRE** for quick access.

---

## 🛠 Usage

### Prerequisites
* Logged into a **Kibana 8.x** instance.
* For alert operations, make sure the **`kibana.alert.uuid`** column is visible in your Alerts table.

### Workflow
1. **Notes & Triage:** Open your Kibana Alerts view, click the **GCRE** icon, type your note, toggle your desired actions (`Add Note`, `add false positive tag`, `close all alerts`, `Reload`), and hit **▶ EXECUTE**.
2. **Delete Notes:** Switch to the **DEL NOTES** tab, click **STEP 1: SCAN & FETCH NOTES**, verify the count, then click **STEP 2: DELETE ALL FOUND NOTES**.
3. **Rule Import:** Switch to the **RULE IMPORT** tab, set your delay and overwrite options, click **OPEN FOLDER IMPORTER HUD ON KIBANA**, and select the folder containing your `.ndjson` rule files.

---

## 👤 Credits
* **Developed by:** GohTM
* **Designed by:** erio & morecha
