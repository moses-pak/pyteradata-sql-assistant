# PyTeradata SQL Assistant

A lightweight, modern take on Teradata SQL Assistant. Two flavors, both standalone —
**no Python, no installs, nothing but a double-click.**

## Download

Grab the latest from the [**Releases page**](https://github.com/moses-pak/pyteradata-sql-assistant/releases/latest), or use these direct links — **the `.zip` versions are recommended** (they let you skip the SmartScreen warning, see *First run* below):

| App | Recommended | Alternative | What it is |
|---|---|---|---|
| 🖥️ Desktop | [Desktop .zip](https://github.com/moses-pak/pyteradata-sql-assistant/releases/latest/download/PyTeradata-SQL-Assistant-Desktop.zip) | [.exe](https://github.com/moses-pak/pyteradata-sql-assistant/releases/latest/download/PyTeradata-SQL-Assistant-Desktop.exe) | Classic desktop app (query editor, results grid, history, explorer) |
| 🌐 Browser | [Web .zip](https://github.com/moses-pak/pyteradata-sql-assistant/releases/latest/download/PyTeradata-SQL-Assistant-Web.zip) | [.exe](https://github.com/moses-pak/pyteradata-sql-assistant/releases/latest/download/PyTeradata-SQL-Assistant-Web.exe) | Same features in your browser — running locally on your machine |

## First run

**Zip route (no SmartScreen warning):**

1. Download the `.zip`.
2. **Before extracting:** right-click the zip → **Properties** → check **Unblock** (bottom right) → **OK**.
   This clears Windows' "downloaded from the internet" flag for everything inside.
3. Right-click → **Extract All**, open the folder, double-click the `.exe`.

**Exe route:** double-click the downloaded `.exe`; if SmartScreen says *"Windows protected your PC"*,
click **More info → Run anyway** (the exes are unsigned; the warning is expected).

Notes for both routes:

- The **first** launch takes ~10 seconds while the app unpacks — after that it's fast.
- Browser version: a console window opens (that's the local server — leave it running), and the app
  opens in your default browser at `http://127.0.0.1:8000`. **Close the console window to quit.**

## Connecting to Teradata

- **Easiest — Teradata native:** in the Connect dialog choose *Teradata native*, enter the Teradata
  host name, your username/password, and the logon mechanism (TD2 or LDAP). Nothing to install.
- **ODBC DSNs:** the app also lists any DSNs from your Windows *ODBC Data Sources (64-bit)*
  Administrator. For Teradata DSNs you need the **64-bit** Teradata ODBC driver installed.

## Features

- SQL editor with syntax highlighting — **F5** runs (selection or whole script), **F6** explains
- Multi-statement scripts, one sortable answerset grid per statement, cancel button
- Query history, kept locally and searchable — double-click to re-run
- Database explorer tree (databases → tables/views/macros → columns) with *Show Definition*
- Export results to CSV/Excel · import CSV files into tables
- Dark mode 🌙 in both apps

## Privacy

Everything runs on your machine. Queries go directly from your PC to your Teradata systems;
history is stored locally in `%APPDATA%\PyTeradataSQLAssistant`. Nothing is sent anywhere else.
