The Pulse
The Pulse | Sectoral Resource Orchestration DPI
The Pulse is a Digital Public Infrastructure (DPI) solution designed for real-time resource orchestration across Agriculture, Healthcare, and Urban Logistics. It synchronizes sectoral surpluses and demands through a geospatial trust layer to reduce waste and optimize emergency response.

Features
1. Geospatial Dashboard: Real-time visualization of resources using Leaflet and OpenStreetMap.
2. Sectoral Registries: Dedicated logic for Agri-Sync (surplus management), Health-Match (emergency assets), and Urban-Flow (logistics).
3. Voice Bridge: Multi-lingual voice interface for field reporting (Farmers/Logistics drivers).
4. DPI Trust Layer: Verifiable data architecture for inter-sectoral interoperability.
5. Responsive UI: Dark-themed, high-performance interface built with Tailwind CSS and Framer Motion.

Tech Stack
Frontend: React.js, Tailwind CSS, Leaflet, Framer Motion, Lucide-React.
Backend: Node.js, Express.js.
Database: MongoDB (via Mongoose).
Real-time: Socket.io (for live Pulse updates).

Setup & Installation
Prerequisites
Node.js (v16.x or higher)
npm or yarn
MongoDB Atlas account or local MongoDB instance

1. Clone and Install
Bash

# Clone the repository
git clone https://github.com/your-username/the-pulse.git
cd the-pulse

# Install Backend Dependencies
cd backend
npm install

# Install Frontend Dependencies
cd ../frontend
npm install
2. Environment Variables
Create a .env file in the backend folder:

Code snippet

PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/thepulse
JWT_SECRET=your_super_secret_key_123
NODE_ENV=development
3. Running Locally
To run the Backend:

Bash
cd backend
npm run dev
To run the Frontend:

Bash
cd frontend
npm run dev
The app should now be running at http://localhost:5173 (Vite) or http://localhost:3000 (CRA).

Test Credentials
If your build includes authentication, use these for testing:

Admin User: admin@thepulse.dpi / admin123
Field Agent: agent@thepulse.dpi / agent123

Error Handling & Troubleshooting
White Screen: Ensure App.css has .leaflet-container { height: 100vh; }. Without a defined height, the map renders at 0px.
URI Malformed: Ensure your project folder path does not contain spaces or special characters (e.g., use the-pulse instead of The Pulse).
Missing Script dev: Ensure your package.json in the frontend/backend folders contains "dev": "react-scripts start" or "dev": "nodemon server.js".
MongoDB Connection: Ensure your IP address is whitelisted in MongoDB Atlas.

Security & Secrets
No Secrets: This repository contains no hardcoded API keys, database credentials, or private tokens.
Gitignore: A .gitignore file is active to prevent .env and node_modules from being committed.
