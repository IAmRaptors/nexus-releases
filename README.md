# N E X U S

A database deck for people who have never touched one.
Made by **Ace Developments** — © 2026.

Browse databases like spreadsheets, edit server tables, write and
run code, and manage remote files — all in one dark, friendly window.

---

## Installing (the easy way)

1. Run **`installer\NexusSetup.exe`**
2. Click through the wizard — you can change the install folder on the
   "Select Destination Location" page
3. Leave **"Create a desktop icon"** checked if you want a desktop shortcut
4. Hit **Install**, then **Launch Nexus**

That's it — Nexus lives in `%LocalAppData%\Programs\Nexus` and shows up
in the Start Menu like any normal app.

### Updating

Run the new `NexusSetup.exe` over the old install. **Your data is safe**
— connections, databases, plugins, settings, and your workspace all live
in `%APPDATA%\Nexus`, completely separate from the program files.
Nothing you own is deleted by an update.

### Uninstalling

Start Menu → Nexus → Uninstall, or Windows Settings → Apps → Nexus.
Your data folder stays behind unless you delete it yourself.

---

## Running without installing (dev build)

`dist4\Nexus\Nexus.exe` — no setup needed, same data folder.

---

## Quick tour

| Rail button | What it does |
|---|---|
| ⌂ HOME | Connections dashboard — every deck you have mounted |
| ✚ ADD | The database catalog — SQLite, MySQL/MariaDB, PostgreSQL, DuckDB, CSV… |
| ▦ DATA | Browse tables, edit cells inline, run SQL |
| ⟳ SYNC | Reload everything |
| `</>` CODE | VS Code-style editor — files, syntax highlighting, SFTP browsing |
| ⚙ SET | Settings — themes, languages, plugins, connections |
| ⬡ DISC | The Discord server |

### Tips

- Data grid edits write immediately — no save button.
- Remote tables need a primary key to be editable (most FiveM tables
  have one). Tables without a PK are view-only — that's a MySQL limit,
  not a Nexus one.
- The CODE tab never touches a database unless you pick one in the
  **"run on:"** dropdown. `no deck` = totally standalone files.
- Plugins: drop a `.py` file into `%APPDATA%\Nexus\plugins` and hit
  Reload in Settings → Plugins.

---

## For developers

```powershell
python nexus.py          # run from source
```

Built with PyQt6. Packaged with PyInstaller (`--onedir --windowed`).
Installer script: `nexus.iss` (Inno Setup 6).

Your data always lives in `%APPDATA%\Nexus` — never next to the exe.

