# GitScope

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> A browser-based GitHub repository visualizer. Explore file structures, commit history, contributors, and more — all without a backend.

![GitScope Screenshot](screenshot.png)
*Screenshot placeholder — replace with actual screenshot*

---

## What It Does

GitScope fetches and visualizes public GitHub repositories directly in your browser. Paste any public repo URL and instantly see:

- **File structure** as an interactive treemap
- **Language breakdown** with donut charts
- **Commit activity** over time
- **Contributor insights** and ownership
- **File intelligence** — abandoned, most changed, and largest files
- **Bus factor warnings** for single-contributor files

No backend, no authentication, no installation required.

---

## Features

### Repo Overview
- Repository name, description, stars, forks, and age
- Total files and contributors
- Language breakdown donut chart (Chart.js)
- Commit frequency bar chart by month (Chart.js)

### Interactive Treemap (D3.js)
- Each file is a rectangle sized by **file size** or **commit count** (toggle)
- Color by **file type/extension**, **top author**, or **recency** (toggle)
- Click folders to drill down; breadcrumb navigation to go back
- Hover tooltips with filename, size, commits, author, and last modified date
- Dynamic legend based on current coloring mode

### Contributor Insights
- Leaderboard with avatar, username, commit count, files owned, and percentage
- Click an author to highlight only their files in the treemap
- **Bus factor warning**: files where only one person has ever committed

### File Intelligence Panel
- **Abandoned files**: not modified in 6+ months
- **Most changed files**: highest commit count
- **Largest files**: by byte size
- Tabbed interface to switch views

### Search & Filter
- Search files by name or extension
- Filter by author, file type, or date range (30d / 6mo / 1yr / all time)
- Real-time updates to treemap and table

### Table View
- Toggle between treemap and sortable table
- Columns: filename, path, size, commits, top author, last modified, type
- Click any column header to sort

### Export & Sharing
- **Copy shareable link**: encodes repo in URL as `?repo=owner/repo`
- **Export treemap as PNG**: saves current visualization

---

## How to Use

### Option 1: Open Locally
1. Download or clone this repository
2. Open `index.html` in any modern browser
3. Paste a GitHub repo URL (e.g., `https://github.com/facebook/react`)
4. Click **Analyze**

### Option 2: GitHub Pages
Visit the hosted version (if deployed) with a direct link:
```
https://your-username.github.io/gitscope/?repo=owner/repo
```

### Option 3: Shareable Links
After analyzing a repo, click **Copy Link** to get a shareable URL that auto-loads the repo.

---

## Deploy to GitHub Pages

1. **Fork this repository** or push to your own GitHub repo

2. **Go to repository Settings** → Pages

3. **Set Source** to `Deploy from a branch`

4. **Select branch**: `main` (or `master`)

5. **Select folder**: `/ (root)`

6. **Click Save**

7. Wait 1-2 minutes for deployment

8. Access your site at:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
   ```

9. Share direct links to repos:
   ```
   https://YOUR-USERNAME.github.io/gitscope/?repo=facebook/react
   ```

---

## GitHub API Rate Limits

GitScope uses the **unauthenticated GitHub REST API**, which has a rate limit of:

| Limit | Value |
|-------|-------|
| Requests per hour | 60 |
| Requests per repo analysis | ~6-8 |

### Tips to Avoid Rate Limits

- ✅ **Use on small to medium repos** (< 5,000 files)
- ✅ **Wait between analyses** if you're testing multiple repos
- ✅ **Use the shareable link feature** to revisit repos without re-fetching
- ⚠️ Large repos with 10,000+ files may hit tree size limits

### When Rate Limited

If you hit the rate limit, GitScope will show an error with the reset time. Wait until the limit resets (usually within an hour).

---

## Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML/CSS/JS** | Core application (no frameworks) |
| **D3.js v7** | Interactive treemap visualization |
| **Chart.js v4** | Donut and bar charts |
| **html2canvas** | Export treemap as PNG |
| **Google Fonts** | Syne (headings) + Space Mono (code/data) |

All libraries loaded from **cdnjs CDN** — no build step required.

---

## Design

- **Dark theme** with `#0a0a0f` background
- **Accent color**: `#e8ff47` (electric yellow-green)
- **Grid pattern** background for visual depth
- **Responsive** down to 768px width
- **Smooth transitions** and hover states throughout

---

## Browser Support

GitScope works in all modern browsers:

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ❌ Internet Explorer (not supported)

---

## Contributing

Contributions are welcome! Here's how:

1. **Fork** this repository
2. **Create a branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes** to `index.html`
4. **Test locally** by opening in a browser
5. **Commit**: `git commit -m 'Add amazing feature'`
6. **Push**: `git push origin feature/amazing-feature`
7. **Open a Pull Request**

### Ideas for Contributions

- [ ] Add dark/light theme toggle
- [ ] Support authenticated API for higher rate limits
- [ ] Add commit history timeline visualization
- [ ] Improve mobile responsiveness
- [ ] Add file content preview on click
- [ ] Support GitLab/Bitbucket repositories

---

## License

This project is licensed under the **MIT License** — see below:

```
MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Acknowledgments

- [GitHub REST API](https://docs.github.com/en/rest) for repository data
- [D3.js](https://d3js.org/) for powerful visualizations
- [Chart.js](https://www.chartjs.org/) for beautiful charts
- [Google Fonts](https://fonts.google.com/) for Syne and Space Mono

---

<p align="center">
  Built with 💚 using vanilla JavaScript
</p>
