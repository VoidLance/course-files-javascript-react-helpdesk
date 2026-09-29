# Helpdesk Ticket Board

A small helpdesk dashboard built with React 19 and Bun. It organizes support tickets by status and lets users create tickets, inspect their details, and delete tickets from the board.

## Features

- View tickets grouped into **Completed**, **In Progress**, and **Failed** columns.
- Create tickets with a name, title, description, date, and status.
- Select a ticket to view its details.
- Delete tickets from the detail view.
- Run a lightweight Bun server with hot module reloading during development.
- Includes example JSON API routes for testing:
  - `GET /api/hello`
  - `PUT /api/hello`
  - `GET /api/hello/:name`

Ticket data is currently held in React component state, so it resets when the page is refreshed. There is no database or authentication layer.

## Prerequisites

- [Bun](https://bun.com) 1.3 or later
- Git

## Getting started

Clone the repository, install dependencies, and start the development server:

```bash
git clone https://github.com/VoidLance/course-files-javascript-react-helpdesk.git
cd course-files-javascript-react-helpdesk
bun install
bun dev
```

Open the URL printed by Bun, typically `http://localhost:3000`, in a browser. Changes to files in `src/` are reflected automatically through hot module reloading.

## Available commands

| Command | Description |
| --- | --- |
| `bun install` | Install dependencies from `bun.lock`. |
| `bun dev` | Start the development server with hot reloading. |
| `bun run build` | Create a minified browser build in `dist/`. |
| `bun start` | Start the Bun server with `NODE_ENV=production`. |

To verify the example API routes while the server is running:

```bash
curl http://localhost:3000/api/hello
curl http://localhost:3000/api/hello/Ada
curl -X PUT http://localhost:3000/api/hello
```

## Project structure

```text
src/
├── App.tsx                  # Ticket state and main dashboard UI
├── components/
│   ├── StatusBoard.tsx      # Status columns
│   ├── TicketInfo.tsx       # Ticket status card wrapper
│   └── APITester.tsx        # Reusable API request tester
├── frontend.tsx             # React entry point
├── index.html               # HTML shell
├── index.ts                 # Bun server and API routes
└── index.css                # Application styles
```

## Support

For bugs or feature requests, [open an issue](https://github.com/VoidLance/course-files-javascript-react-helpdesk/issues). For framework and runtime documentation, see the [React documentation](https://react.dev/learn) and [Bun documentation](https://bun.com/docs).

## Contributing

Contributions are welcome. Before opening a pull request:

1. Create a focused branch for your change.
2. Run `bun install` and `bun run build`.
3. Test the affected ticket flows and API routes locally.
4. Describe the change and validation steps in your pull request.

Please keep changes focused and update this README when setup or user-facing behavior changes.

## Maintainer

This project is maintained by [VoidLance](https://github.com/VoidLance) and its contributors.
