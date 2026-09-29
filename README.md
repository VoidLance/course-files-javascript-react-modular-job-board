# Job Board

A small, modular job-board application built with React, TypeScript, and Bun. It provides a simple interface for managing jobs in memory while demonstrating how a Bun server can serve a React frontend and JSON API routes from one project.

## Why use this project?

- Add jobs with a name and `running` or `completed` status.
- Show or hide the job list without leaving the page.
- Filter the list by status.
- Edit or delete existing jobs.
- Run the frontend and Bun API server together with hot module reloading during development.
- Use the included API routes as a starting point for connecting a persistent backend.

Jobs are currently stored in React state, so refreshing the page resets the sample data. The project is intentionally small and suitable for learning, experimentation, and extending into a full job-management application.

## Getting started

### Prerequisites

- [Bun](https://bun.com) 1.x or newer
- Git

### Installation

Clone the repository, enter the project directory, and install dependencies:

```bash
git clone https://github.com/VoidLance/course-files-javascript-react-modular-job-board.git
cd course-files-javascript-react-modular-job-board
bun install
```

### Development

Start the development server with hot reloading:

```bash
bun dev
```

Open the URL printed by Bun in your browser. The application starts with sample jobs. Use the form to add a job, then use the list controls to filter, edit, or delete it.

### Production build

Create an optimized browser bundle:

```bash
bun run build
```

Run the server in production mode:

```bash
bun start
```

The generated bundle is written to `dist/`.

## API examples

The Bun server exposes a small example API:

```bash
# GET /api/hello
curl http://localhost:3000/api/hello

# PUT /api/hello
curl -X PUT http://localhost:3000/api/hello

# Parameterized greeting
curl http://localhost:3000/api/hello/Ada
```

The API returns JSON responses such as:

```json
{
  "message": "Hello, Ada!"
}
```

API routes are defined in [`src/index.ts`](src/index.ts). The React application starts in [`src/App.tsx`](src/App.tsx), with reusable UI pieces in [`src/components`](src/components).

## Project structure

```text
src/
├── components/       Reusable header, footer, list, and job item components
├── App.tsx           Job state and page-level interactions
├── frontend.tsx      React entry point
├── index.html        HTML document entry point
├── index.ts          Bun server and API routes
└── index.css         Application styles
```

## Support

For questions or problems:

1. Check the setup and API examples above.
2. Search [existing issues](https://github.com/VoidLance/course-files-javascript-react-modular-job-board/issues).
3. [Open an issue](https://github.com/VoidLance/course-files-javascript-react-modular-job-board/issues/new) with a clear description, reproduction steps, and relevant environment details.

## Contributing

Contributions are welcome. Fork the repository, create a focused branch, make your change, and open a pull request describing what changed and how it was checked. Keep changes focused and update this README when setup or user-facing behavior changes.

## Maintainer

This project is maintained by [VoidLance](https://github.com/VoidLance).
