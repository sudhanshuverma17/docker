# Live Code Editor

A real-time collaborative code editor that enables multiple users to edit the same code simultaneously. The application uses CRDT-based synchronization through Yjs and Socket.IO to provide seamless collaboration with automatic conflict resolution.

## Features

- Real-time collaborative code editing
- Multi-user editing support
- Automatic synchronization across connected clients
- Conflict-free document updates using Yjs
- Monaco Editor integration for a VS Code-like editing experience
- Responsive user interface
- Docker support for containerized deployment
- Cross-device compatibility

## Tech Stack

### Frontend

- React
- Vite
- Monaco Editor
- Yjs
- y-monaco
- Socket.IO Client
- CSS

### Backend

- Node.js
- Express.js
- Socket.IO
- Yjs
- y-socket.io

### Deployment

- Docker
- AWS ECS

## Project Structure

```text
live-code-editor/
├── client/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── server/
│   ├── server.js
│   ├── routes/
│   └── package.json
│
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Installation

### Clone the repository

```bash
git clone https://github.com/your-username/live-code-editor.git
cd live-code-editor
```

### Install dependencies

For the client:

```bash
cd client
npm install
```

For the server:

```bash
cd ../server
npm install
```

## Running the Application

Start the backend server:

```bash
cd server
npm run dev
```

Start the frontend:

```bash
cd client
npm run dev
```

Open the application in your browser at:

```
http://localhost:5173
```

## Running with Docker

Build the Docker image:

```bash
docker build -t live-code-editor .
```

Run the container:

```bash
docker run -p 3000:3000 live-code-editor
```

## How It Works

1. Users connect to the same collaboration session.
2. Monaco Editor provides the code editing interface.
3. Yjs synchronizes document changes using CRDTs.
4. Socket.IO transmits updates between connected clients.
5. All users receive changes instantly without merge conflicts.

## Future Enhancements

- User authentication
- Multiple programming language support
- Code execution
- File explorer
- Chat functionality
- Session persistence
- Cursor presence indicators
- Theme customization
- Code formatting and linting

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.

```bash
git checkout -b feature-name
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push to your branch.

```bash
git push origin feature-name
```

5. Open a Pull Request.

## Author

Sudhanshu Verma
