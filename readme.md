# Daylight

A responsive daily planner with tasks, categories and due dates, daily habits, a focus timer, and an autosaved daily note. Built with HTML, CSS, and JavaScript, with no build step or runtime dependencies.

Live app: https://naveenalavilli.github.io/daylight/

Source: https://github.com/naveenalavilli/daylight

## Run locally

Requires Node.js. Run `npm run dev`, then open http://127.0.0.1:5187.

Run `npm run check` to check JavaScript syntax.

## Deploy to GitHub Pages

Push changes to `main`. The workflow in `.github/workflows/pages.yml` checks JavaScript syntax and deploys the `public` directory to GitHub Pages. You can also start it manually from the repository's Actions tab.

In repository Settings → Pages, the deployment source is **GitHub Actions**. No build step, API key, or deployment secret is needed. Relative asset URLs support the `/daylight/` project path.

## Data and behavior

- Tasks, habits, notes, and completed focus minutes are stored in this browser's localStorage, under `daylight-v1`. Data does not sync between devices or between the local and deployed URLs. Clearing browser data removes it.
- My day includes tasks due today, unfinished overdue tasks, and tasks completed today. All tasks also includes future tasks.
- Habits, notes, and focus totals are tracked separately for each local calendar date. The app switches dates when left open overnight.
- The timer uses a timestamp to account for browser throttling. Keep the tab open to finish a session; refreshing or closing it resets the running timer. A five-minute break does not count toward focus minutes.
- Fonts come from Google Fonts, with system sans-serif fallbacks.

Browser checks performed using the connected Nabsun browser: task creation and completion, active/completed filtering, habit toggles, notes saved across reload, timer duration changes, start, pause, and reset. The current 538px-wide browser view has no horizontal overflow.
