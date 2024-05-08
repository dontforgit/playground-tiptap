# Tiptap Playground with Vite and Vue

This repository is a playground for experimenting with the Tiptap rich text editor using Vue 3 and Vite. Tiptap is a headless editor framework that provides a clean and extensible architecture which allows you to build your own rich text editor based on ProseMirror.

## Features

- Rich text editing using Tiptap with a variety of extensions.
- Collaboration features using `y-prosemirror`, `y-webrtc`, and `yjs`.
- Development environment powered by Vite and Vue 3.

## Prerequisites

Before you start, make sure you have the following installed:
- Node.js (v18.x)
- npm (v8.x) or Yarn (v1.x)

This project uses Yarn as the package manager, as indicated by the presence of a `yarn.lock` file. If you prefer npm, you should be able to follow along, but make sure to generate your own `package-lock.json`.

## Getting Started

To get the project running on your local machine, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/tiptap-test.git
   cd tiptap-test
   ```
   
2. Install dependencies:

    Using Yarn:

   ```bash
   yarn install
   ```

   Using npm:

   ```bash
   npm install
   ```

3. Start the development server

    Using Yarn:

   ```bash
   yarn dev
   ```

   Using npm:

   ```bash
   npm run dev
   ```

    This command will start the Vite development server at http://localhost:3000. Open this URL in your browser to see your Tiptap editor in action.

4. Build the project (optional):To build the application for production, use:
    
    Using Yarn:
    
    ```bash
    yarn build
    ```
    
    Using npm:

    ```bash
    npm run build
    ```
    
    This command will generate a `dist` folder containing the production-ready build of your application.

## Directory Structure
 - `src/`: Contains the Vue component files and other source files.
- `index.html`: The entry point for the application which includes the  main Vue app mounting.
- `vite.config.js`: Configuration for the Vite build tool.
