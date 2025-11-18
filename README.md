

# Real-time 3D Avatar Simulation from Facial Expressions
> ### PBL6 Project: 3D Model Simulation based on Facial States

## 👥 Contributors

| Name                   | GitHub                                             | Role                       |
| ---------------------- | -------------------------------------------------- | -------------------------- |
| **Lê Đức Phúc Long**   | [@leducphuclong](https://github.com/leducphuclong) | Team Lead, AI/ML Integration |
| Nguyễn Nhật Huy      | [@ntgcmfy · he/him](https://github.com/ntgcmfy) | Front-end Development      |
| Trần Ngọc Minh Hoàng | [@Ahrumiki](https://github.com/Ahrumiki)       | Back-end Development       |


## 📘 Introduction
This project is a web-based platform that allows users to control 3D avatars in real-time using their own facial expressions. The system captures facial movements through a webcam and maps them onto a virtual character, creating an immersive and personalized experience.

The core feature is a **Vtuber-style video calling system** where users interact through their animated avatars instead of their real faces, ensuring privacy while offering a fun and engaging communication tool.

## ✨ Key Highlights
*   **Real-time Facial Tracking:** Low-latency mapping of facial expressions (smiling, blinking, mouth movements, head tilts) to the 3D model.
*   **Custom 3D Avatar Support:** Users can select from a default library or upload their own models in `GLTF`, `FBX`, and `VRM` formats.
*   **WebRTC-Powered Video Calls:** High-quality, peer-to-peer video and audio streaming for a seamless communication experience.
*   **Privacy-Focused:** Facial processing is handled client-side or end-to-end encrypted. No raw video or image data is stored on the server without explicit user consent.
*   **Dynamic Call Experience:** Features include text chat, video recording, and customizable call window layouts (Grid, Focus, Fullscreen).

## 🔑 Core Features

#### 🎭 Facial Expression Control
*   Uses the webcam to detect and track facial landmarks.
*   Translates facial data into corresponding movements on the 3D avatar.
*   Supports key expressions: smiling, sadness, mouth opening, eye blinking, and head tilting.

####  avatars/ Model Management
*   Upload, preview, and manage a personal library of 3D models.
*   Select an active avatar for use in video calls.
*   Set a default avatar that loads automatically upon login.

#### 📞 Video Calling (Vtuber Mode)
*   Create or join video call rooms.
*   Your avatar appears in the call, mimicking your expressions in real-time.
*   Live text chat functionality during calls.
*   Record video sessions and save them locally.
*   Manage room participants (view list, host controls).

#### 🔐 Account Management
*   Secure user registration and login system.
*   Email verification and a "Forgot Password" recovery flow.
*   Users can edit their personal profile information.

## 🛠️ Technologies Used

#### **Frontend**
*   **React** (or a similar modern JS framework)
*   **Three.js / Babylon.js** (for 3D rendering in the browser)
*   **MediaPipe / TensorFlow.js** (for facial landmark detection)
*   **WebRTC** (for real-time communication)
*   **HTML5** & **CSS3**

#### **Backend**
*   **Node.js** with **Express.js**
*   **Socket.IO** (for WebRTC signaling and real-time events)
*   **PostgreSQL** (Database)
*   **Prisma** or **Sequelize** (ORM for database interaction)

## 📁 Project Structure (Example)
```
avatar-simulation-platform/
├── client/                     # Frontend React App
│   ├── public/
│   └── src/
│       ├── components/         # Reusable UI components
│       ├── hooks/              # Custom React hooks
│       ├── services/           # Face tracking, WebRTC logic
│       └── pages/              # Main pages (Login, Room, Dashboard)
├── server/                     # Backend Node.js App
│   ├── src/
│   │   ├── controllers/        # Request handlers
│   │   ├── models/             # Database schemas
│   │   ├── routes/             # API endpoints
│   │   └── services/           # Business logic
│   └── index.js                # Server entry point
└── README.md
```

## ⚙️ Setup Guide

#### **Prerequisites**
*   **Node.js** v18+
*   **PostgreSQL** 14+
*   **npm** or **yarn** package manager

#### **Step 1: Clone Repository**
```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

#### **Step 2: Configure Database**
1.  Create a new PostgreSQL database.
2.  Navigate to the `server/` directory and create a `.env` file.
3.  Add your database connection string to the `.env` file:
    ```env
    DATABASE_URL="postgresql://YOUR_USER:YOUR_PASSWORD@localhost:5432/YOUR_DATABASE"
    ```4.  Run database migrations (if using an ORM).

#### **Step 3: Install Dependencies**
```bash
# Install backend dependencies
cd server
npm install

# Install frontend dependencies
cd ../client
npm install```

#### **Step 4: Run the Application**
```bash
# Run the backend server (from the server/ directory)
npm start

# Run the frontend application (from the client/ directory)
npm start
```
The application should now be running on `http://localhost:3000`.

## 📊 Usage Guide
1.  **Register & Login:** Create an account and log in to the platform.
2.  **Manage Avatars:** Go to the dashboard to upload a custom 3D model or select one from the library.
3.  **Start a Call:** Create a new room and share the link with others, or join an existing room.
4.  **Enable Camera:** Grant camera permissions to start tracking your facial expressions. Your avatar will come to life!
5.  **Interact:** Chat and talk with others through your animated avatar.

## 📝 License
This project is licensed under the **MIT License**.
