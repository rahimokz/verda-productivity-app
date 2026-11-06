# VERDA

> Plan Smarter. Stay Focused. Get Things Done.

VERDA is a local-first productivity workspace for planning tasks, tracking projects, and protecting focus time. It is designed as a polished portfolio-ready SaaS interface while keeping the personal workspace fully usable without an API key or backend account.

## Features

- Dashboard with live task statistics, daily progress, deadlines, and activity chart
- Task creation and editing with status, priority, due date/time, project, and descriptions
- Search palette with `Ctrl/Cmd + K`
- Task filtering and completion controls
- Drag-and-drop Kanban board
- Projects with progress derived from real tasks
- Timestamp-based Pomodoro focus timer
- Analytics based on current workspace data
- Light/dark themes and responsive mobile layout
- LocalStorage persistence and JSON export
- Demo workspace restore flow

## Stack

React, TypeScript, Vite, Zustand, Framer Motion, Lucide React, Recharts, Sonner, and date-fns.

## Run locally

```bash
npm install
npm run dev
```

Quality checks:

```bash
npm run build
npm run lint
```

## Architecture

- `src/App.tsx` contains the typed local-first store, screens, reusable UI, and interactions.
- `src/index.css` contains the responsive design system and light/dark theme tokens.

The Zustand store is the storage boundary. It currently uses LocalStorage and can be replaced with a remote service without changing the page-level UI contract.

## Data and privacy

VERDA does not provide fake authentication and does not transmit workspace data. Tasks and theme/profile preferences stay in the browser's LocalStorage. JSON export creates a local file from the current workspace.

## Deployment

The production bundle is Vercel-compatible:

1. Import the repository into Vercel.
2. Use `npm run build` as the build command.
3. Use `dist` as the output directory.

No environment variables are required for the local-first version.

## Future improvements

Calendar month/week views, recurring tasks, validated JSON import, richer activity history, and a backend sync adapter are natural next steps.

## License

This project is available for portfolio and educational use.
