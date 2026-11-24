# Crextio — Contextual Dashboard

![Crextio dashboard preview](docs/dashboard-preview.png)

A responsive, modern dashboard UI with a warm cream-and-charcoal color palette, inspired by the Crextio dashboard reference. It includes interactive dashboard sections, contextual filters, task management, a performance chart, search, and a persistent light/dark theme.

<p align="center">
  <a href="https://github.com/khdxsohee/crextio">
    <img src="https://img.shields.io/badge/Repo-Crextio-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub repository">
  </a>
  <img src="https://img.shields.io/badge/HTML5-Ready-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-Responsive-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=for-the-badge&logo=javascript&logoColor=222" alt="JavaScript">
  <img src="https://img.shields.io/badge/Chart.js-Visualizations-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white" alt="Chart.js">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
</p>

## About

Crextio is a lightweight, single-page dashboard UI for viewing workspace activity and project information. The interface adapts to mobile screens and lets users switch between dashboard views without reloading the page.

The current dashboard uses **sample data** for its metrics, activity feed, projects, and chart. Connect it to your own API or data source to use real workspace data.

## Features

- **Sidebar sections:** Overview, Analytics, Projects, Tasks, and Team each show their relevant dashboard cards.
- **Context filters:** Quickly switch between Overview, My work, Team, Projects, and This week.
- **Dashboard search:** Search visible dashboard cards by their text.
- **Performance chart:** View sample revenue and task data across different time ranges.
- **Task management:** Add tasks, mark tasks complete, reopen them, and see the remaining-task count update.
- **Theme toggle:** Switch between light and dark themes. The selected theme is saved in browser `localStorage`.
- **Responsive layout:** The sidebar and cards adapt to smaller screens.
- **No build step:** Runs as a static HTML page.

## Getting started

### Option 1: Open the HTML file

1. Clone the repository:

   ```bash
   git clone https://github.com/khdxsohee/crextio.git
   ```

2. Open the project folder:

   ```bash
   cd crextio
   ```

3. Open `index.html` in your browser.

The dashboard is a static page, so no package installation or build command is required.

### Option 2: Run a local development server

If you have Python installed, run:

```bash
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

You can also use another static-file server or your editor’s local preview extension.

## Usage

### Navigate dashboard sections

Use the left sidebar to switch between:

| Section | Dashboard content |
| --- | --- |
| Overview | All dashboard cards |
| Analytics | Metric cards and performance chart |
| Projects | Project progress |
| Tasks | Task list and task controls |
| Team | Recent activity |

### Filter by context

Use the context chips below the page heading to filter the dashboard:

- **Overview** — show all cards.
- **My work** — show personal metrics, chart, and tasks.
- **Team** — show workspace metrics and recent activity.
- **Projects** — show metrics and project progress.
- **This week** — show metrics, chart, and tasks.

### Manage tasks

Select **＋ Add task** to add a task. Use its checkbox to mark it complete or reopen it. The number of remaining tasks updates automatically.

### Change the date range

Use the date-range selector above the dashboard to update the chart’s displayed labels and sample values.

### Switch theme

Select **Toggle theme** in the sidebar. The choice is saved locally in the browser for the next visit.

## Project structure

```text
crextio/
├── index.html
├── README.md
└── docs/
    └── dashboard-preview.png   # Optional screenshot
```

If your repository uses a different file layout, update this section to match it.

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- [Chart.js](https://www.chartjs.org/) for the performance chart

Chart.js is loaded from a CDN in `index.html`, so an internet connection is needed for the chart to appear. The rest of the page is built with standard HTML, CSS, and JavaScript.

## Customization

### Update dashboard content

Edit the metric, activity, task, and project elements in `index.html` to change the displayed content.

### Change the color palette

The main theme colors are defined as CSS custom properties near the top of the `<style>` block:

```css
:root {
  --bg: #e6e6e1;
  --surface: #f8f7f0;
  --text: #292a28;
  --muted: #85847b;
  --accent: #d5c759;
}
```

The dark theme uses a separate set of variables under:

```css
body.dark {
  /* Dark theme colors */
}
```

### Connect real data

The current values are static demo data. To connect a backend:

1. Fetch your dashboard data from your API.
2. Replace the sample metric values with the returned values.
3. Populate the task, project, and activity sections from API responses.
4. Update the chart datasets with real time-series data.
5. Add appropriate loading, error, and empty states.

Do not place private API keys or credentials in client-side JavaScript. Use a backend service for secrets.

## Browser support

The dashboard uses modern browser features, including CSS Grid, CSS custom properties, and `localStorage`. Use a current version of Chrome, Firefox, Safari, or Edge for the best experience.

## Contributing

Contributions, bug reports, and suggestions are welcome.

1. Fork the repository.
2. Create a branch for your change:

   ```bash
   git checkout -b feature/your-change
   ```

3. Make and test your changes in a browser.
4. Commit your work:

   ```bash
   git commit -m "Add your change"
   ```

5. Push the branch and open a pull request.



