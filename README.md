# JavaScript React Helpdesk

A small helpdesk dashboard built with React, TypeScript, and Bun. The app displays tickets grouped by status and lets users create, inspect, and delete tickets in the browser. It also includes a lightweight Bun server with example API routes for testing frontend-to-backend requests.

## Features

- View tickets grouped into **Completed**, **In Progress**, and **Failed** columns.
- Create tickets with a name, title, description, date, and status.
- Select a ticket to view its details or delete it.
- Run a Bun development server with hot module reloading.
- Use the example `/api/hello` routes to experiment with `GET`, `PUT`, and path parameters.
- Build an optimized browser bundle with Bun.

Ticket data currently lives in React state, so changes are reset when the page is reloaded. The project does not yet include authentication, persistence, or a database.

## Requirements

- [Bun](https://bun.com) 1.3 or newer
- A modern browser

## Getting started

Clone the repository and install its dependencies:

```bash
git clone https://github.com/VoidLance/course-files-javascript-react-helpdesk.git
cd course-files-javascript-react-helpdesk
bun install
```

Start the development server:

```bash
bun run dev
```

Open the URL printed by Bun, then use **Create Ticket** to add a ticket. Select any ticket title to view its details.

## Available commands

| Command | Purpose |
| --- | --- |
| `bun run dev` | Start the development server with hot module reloading. |
| `bun run build` | Create a minified browser bundle in `dist/`. |
| `bun run start` | Start the server with `NODE_ENV=production`. |

## Example API requests

The Bun server exposes these example endpoints while it is running:

```bash
# Basic greeting
curl http://localhost:3000/api/hello

# PUT requests are supported too
curl -X PUT http://localhost:3000/api/hello

# Include a name in the greeting
curl http://localhost:3000/api/hello/Ada
```

The response is JSON. The server port is selected by Bun and is shown in the terminal when the server starts; update the examples if your local URL uses a different port.

## Project structure

```text
src/
├── App.tsx                  # Ticket state and main dashboard
├── components/
│   ├── APITester.tsx        # Small UI for trying API endpoints
│   ├── StatusBoard.tsx      # Ticket status columns
│   └── TicketInfo.tsx       # Ticket status presentation
├── frontend.tsx             # React entry point
├── index.css                # Application styles
└── index.ts                 # Bun server and API routes
```

## Support

For questions or bug reports, [open an issue](https://github.com/VoidLance/course-files-javascript-react-helpdesk/issues) with steps to reproduce the problem and relevant browser or terminal output. Review existing issues before opening a new one.

## Maintainers and contributing

This project is maintained by [VoidLance](https://github.com/VoidLance). Contributions are welcome:

1. Fork the repository and create a focused branch.
2. Make the change and verify it with `bun run build`.
3. Open a pull request describing the problem, solution, and verification performed.

Keep changes focused, preserve the existing Bun/React setup, and update this README when user-facing commands or behavior change.

## License

No license file is currently included in the repository. Contact the maintainer before redistributing the project.
