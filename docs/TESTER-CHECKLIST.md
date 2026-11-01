# Friend testing checklist: installation check on another computer (about 10 minutes)

Thank you for helping. The goal is to check that Execution Cockpit installs and starts on a normal Windows
computer **without Python, Git, Node.js or other developer tools**. You do not need to place any orders.

**Testing is free: no payment is needed at any step. Never send money or cryptocurrency for this preview.**

Please note **OK** or **Problem** for each step, and take a screenshot of anything unexpected.

| # | Step | Expected |
|---|---|---|
| 1 | Settings → System → About: note the Windows edition and version | Windows 10 or 11, 64-bit |
| 2 | Optional: in Command Prompt, run `where python` | Ideally "Could not find files". The program must not need Python |
| 3 | Download `ExecutionCockpit-0.5.0-staging-Setup.exe` from the link you were given | 39.2 MB file in Downloads; note any browser warning |
| 4 | In PowerShell: `Get-FileHash "$env:USERPROFILE\Downloads\ExecutionCockpit-0.5.0-staging-Setup.exe"` | `EC3A309A1402E86312ACE37A938551F63B5E16A4CA65511363CB6CBADA95B60A` |
| 5 | Double-click the installer | "Windows protected your PC" is expected: **More info → Run anyway**. **No** administrator (UAC) prompt. Note any antivirus message |
| 6 | On the **License Agreement** page, click **View License Agreement** | The complete agreement opens in your web browser. It does not open by itself before you click |
| 7 | Back in the installer: try **Next** before ticking, then tick **I have read and accept the License Agreement** | **Next** stays greyed out until the box is ticked |
| 8 | Continue with the defaults, finish with *Start Execution Cockpit* ticked | Installs into `%LOCALAPPDATA%\Programs\Execution Cockpit`; the program window opens within about 15 seconds; the User Guide opens in the browser |
| 9 | Look in the Start menu and on the desktop | Folder **Execution Cockpit** with *Execution Cockpit*, *User Guide*, *Uninstall Execution Cockpit*; a desktop shortcut |
| 10 | In the program, click **Account** | The License window opens. The license chip says there is no license yet |
| 11 | Close the program and start it again from the Start menu | It starts again normally |
| 12 | Optional, only with IBKR **Paper** TWS running (API enabled, port 7497): choose Paper, click **Connect** | The status shows the API connected. No orders needed |
| 13 | Optional: **Start free trial on this computer** in the License window | The chip shows a 7-day trial. This uses the one trial for that computer |
| 14 | Optional: Settings → Apps → Installed apps → Execution Cockpit → Uninstall | Program and shortcuts are removed |

Send back the table with OK/Problem, the screenshots, and the Windows version from step 1. Do not send passwords,
account numbers or anything from `%LOCALAPPDATA%\ExecutionCockpit\license`.
