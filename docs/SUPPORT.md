# Support (Public Preview)

Support during the Public Preview is best effort. Your reports decide what gets fixed before the commercial release,
so they are very welcome.

## Report a problem or ask a question

On the Execution Cockpit download page on GitHub, open the **Issues** tab and click **New issue** (a free GitHub
account is needed). If the person who shared the download with you gave you another way to reach us, you can use
that instead.

Please include:

* your Windows version (Settings → System → About) and whether you use TWS or IB Gateway, with its version;
* Paper or Live;
* what you did, what you expected and what happened, with the time and your time zone;
* a screenshot of any message.

## Keep private things private

Issues on GitHub are **public**. Do not post:

* account numbers, e-mail addresses, passwords or recovery phrases;
* your activation key or anything from `%LOCALAPPDATA%\ExecutionCockpit\license`;
* log files. If logs would help, we will ask and arrange a private way to send them. They are in
  `%LOCALAPPDATA%\ExecutionCockpit\logs`.

Nobody from Execution Cockpit will ever ask for your passwords, recovery phrases or the license folder.

## Security problems

If you find a security problem, do not describe it in a public issue. Open an issue that only asks for a private
contact, and we will reply.

## Before you report

* **Connect fails:** is TWS or IB Gateway running and logged in, with API socket clients enabled? Does Paper/Live
  in the Cockpit match the port (7497 / 7496)? Is another program using client ID 73?
* **Orders refused as read-only:** untick *Read-Only API* in the TWS API settings.
* **No prices, or quote-priced orders refuse:** the symbol needs a real-time market-data subscription in your
  IBKR account.
* **"No valid license on this computer":** start the trial or activate a key ([Licensing](LICENSING.md)). Exits
  keep working meanwhile.

More in the User Guide, section 12 "Troubleshooting" (Start menu → Execution Cockpit → User Guide).
