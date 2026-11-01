# Installing Execution Cockpit 0.5.0 (Public Preview)

About 5 minutes. No administrator rights, and nothing else to install: no Python, Git or other tools.

## Before you start

* Windows 10 or 11, 64-bit, about 300 MB free disk space, a screen at least 1280 pixels wide.
* An Interactive Brokers account, and TWS or IB Gateway on the same computer. We recommend an IBKR **Paper**
  account while you try the program.

## 1. Download

Download `ExecutionCockpit-0.5.0-staging-Setup.exe` (39.2 MB) from the official Execution Cockpit release page on
GitHub, or from the link you were given. Do not run copies from anywhere else.

## 2. Check the download (recommended)

Open PowerShell (Start menu → type *PowerShell*) and run:

```powershell
Get-FileHash "$env:USERPROFILE\Downloads\ExecutionCockpit-0.5.0-staging-Setup.exe"
```

The `Hash` value must be exactly:

```
EC3A309A1402E86312ACE37A938551F63B5E16A4CA65511363CB6CBADA95B60A
```

(PowerShell shows it in capitals; `SHA256SUMS.txt` has the same value in lower case.) If it differs, do not run
the file: download it again from the official page.

## 3. Run the installer

1. Double-click the installer.
2. Windows may show **"Windows protected your PC"** (SmartScreen). This happens because the preview installer is
   not code-signed yet, so its publisher shows as unknown. **If the checksum in step 2 matched**, click
   **More info → Run anyway**. Never do this for a file you have not checked.
3. The installer's pages:
   * **Welcome**: close Execution Cockpit first if it is running.
   * **License Agreement**: a short summary. **View License Agreement** opens the complete agreement in your web
     browser. Tick **I have read and accept the License Agreement**, then click **Next**. The agreement is
     preliminary, pending professional legal review; it is published with the download and installed with the
     program.
   * **Choose Components**: the program (always) and a desktop shortcut (untick it if you do not want one).
   * **Choose Install Location**: keep `%LOCALAPPDATA%\Programs\Execution Cockpit`, your own user folder, so no
     administrator rights are needed.
   * **Completing**: *Start Execution Cockpit* and *Open the User Guide*.

The Start menu then has an **Execution Cockpit** folder with *Execution Cockpit*, *User Guide* and
*Uninstall Execution Cockpit*. Installing is for your Windows user only.

If your antivirus program blocks the installer, first check the SHA-256 (step 2). New programs without a code
signature are sometimes flagged by mistake. Please tell us ([Support](SUPPORT.md)) and do not turn off your
antivirus.

## 4. Prepare TWS or IB Gateway (once)

In TWS: **File (or Edit) → Global Configuration → API → Settings**:

* tick **Enable ActiveX and Socket Clients**;
* untick **Read-Only API** (the Cockpit places orders);
* socket port **7497** for Paper or **7496** for Live (the TWS defaults);
* keep **Allow connections from localhost only** ticked. Apply and OK.

IB Gateway uses ports 4002 / 4001 by default. Set them to 7497 (Paper) or 7496 (Live) in **Configure → Settings →
API → Settings**. Execution Cockpit connects with API client ID **73**, so give any other API program a different ID.

## 5. First start

1. Start Execution Cockpit from the Start menu or the desktop shortcut.
2. Choose **Paper** or **Live** to match the TWS you logged in to, then click **Connect**.
3. If it asks for your trading account, use **SET UP ACCOUNT…** and pick the account it should trade.
4. Get a license for new entries: [Licensing and activation](LICENSING.md).

## Updating

Close Execution Cockpit (make sure no order is in flight), run the new installer and keep the same install location.
Your settings, accounts, hotkeys, safety records and license stay as they were.

## Uninstalling

**Settings → Apps → Installed apps → Execution Cockpit → Uninstall**, or Start menu → Execution Cockpit →
*Uninstall Execution Cockpit*. This removes the program and its shortcuts. It keeps your data in
`%LOCALAPPDATA%\ExecutionCockpit` (settings, safety records, logs and this computer's license), so a reinstall
continues where you left off. Delete that folder by hand only if you want to remove everything, and only when you
have no open positions.

The full User Guide is installed with the program (Start menu → Execution Cockpit → User Guide).
