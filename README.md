# Full-Stack-Engineer
Assessment for Full-Stack Engineer 

# MERN Stack Developer Assessment Test
## Objective
Create a real-time chat application with video call functionality to demonstrate proficiency in the MERN stack, WebRTC, Socket.io, and NestJS. The application should allow users to register, log in, create/join chat rooms, send text messages, and initiate video calls. The task should be completed within 8 hours.

## Requirements
- **Frontend**: Build a React-based SPA with a responsive UI for user authentication, chat room management, messaging, and video call interface.
- **Backend**: Use NestJS with Express.js for RESTful APIs and Socket.io for real-time messaging. Implement WebSocket for real-time updates.
- **Database**:
  - Use MySQL for storing user credentials and chat room metadata.
  - Use MongoDB (NoSQL) for storing chat messages.
- **Real-Time Features**: Implement WebRTC for peer-to-peer video calls and Socket.io for real-time chat.
- **Security**: Implement JWT-based authentication for APIs and secure WebSocket connections.
- **Testing**: Write basic unit tests for at least one backend service and one frontend component.
- **Documentation**: Provide a README with setup instructions, API endpoints, and a brief explanation of the architecture.

## Tasks
1. **User Authentication**:
   - Create registration and login endpoints (`POST /api/auth/register`, `POST /api/auth/login`).
   - Store user data (username, hashed password) in MySQL.
   - Return a JWT token upon successful login.

2. **Chat Room Management**:
   - Allow users to create and join chat rooms (`POST /api/rooms`, `GET /api/rooms`).
   - Store room metadata (name, creator, created_at) in MySQL.
   - Display a list of available rooms in the frontend.

3. **Real-Time Messaging**:
   - Implement a Socket.io-based messaging system for real-time text chats within rooms.
   - Store messages in MongoDB with fields: `roomId`, `userId`, `message`, `timestamp`.
   - Display messages in the frontend with sender details and timestamps.

4. **Video Call Feature**:
   - Implement WebRTC for peer-to-peer video calls between two users in a room.
   - Create a simple UI button to initiate/leave a call.
   - Handle signaling via WebSocket (using Socket.io).

5. **Backend APIs**:
   - Use NestJS to create RESTful APIs for authentication, room management, and message history retrieval.
   - Secure APIs with JWT authentication.
   - Implement WebSocket endpoints for real-time updates (e.g., new message notifications).

6. **Frontend Features**:
   - Build a React SPA with components for:
     - Login/Register forms.
     - Chat room list and creation form.
     - Chat window with message input and display.
     - Video call interface with start/stop buttons.
   - Use a CSS framework (e.g., Tailwind CSS) for styling.
   - Ensure the UI is responsive and user-friendly.

7. **Testing**:
   - Write unit tests for the authentication service in NestJS (e.g., validate login functionality).
   - Write a unit test for a React component (e.g., message display component) using Jest.

8. **Deployment Instructions**:
   - Provide a README with:
     - Setup instructions (e.g., environment variables, database setup).
     - List of API endpoints and their purposes.
     - Brief explanation of the WebRTC signaling process.
     - Instructions to run tests.

## Tech Stack
- **Frontend**: React, Tailwind CSS, Socket.io-client, Simple-Peer (for WebRTC)
- **Backend**: NestJS, Express.js, Socket.io, JWT
- **Databases**: MySQL (user and room data), MongoDB (messages)
- **Real-Time**: WebRTC, Socket.io, WebSocket
- **Testing**: Jest (for React and NestJS)
- **Other**: TypeScript (optional but preferred), Git

## Evaluation Criteria
- **Functionality**: All features (authentication, chat, video call) work as expected.
- **Code Quality**: Clean, modular, and well-organized code with proper error handling.
- **Real-Time Implementation**: Effective use of Socket.io and WebRTC for messaging and video calls.
- **Database Usage**: Correct use of MySQL and MongoDB for respective data types.
- **Security**: Proper JWT implementation and secure WebSocket connections.
- **Testing**: Presence of meaningful unit tests.
- **Documentation**: Clear and concise README with all required details.
- **UI/UX**: Responsive and intuitive frontend design.

## Submission
- Share a GitHub repository with the complete codebase.
- Include a README with setup and testing instructions.
- Provide a live demo link (if possible, e.g., hosted on Vercel/Heroku) or a video walkthrough of the application.

## Sample File Structure
```
mern-chat-app/
├── client/                       # React frontend
│   ├── src/
│   │   ├── components/          # React components (e.g., ChatWindow, VideoCall)
│   │   ├── pages/               # Pages (e.g., Login, Rooms)
│   │   ├── App.tsx
│   │   └── index.tsx
├── server/                       # NestJS backend
│   ├── src/
│   │   ├── auth/                # Authentication module
│   │   ├── rooms/               # Chat room module
│   │   ├── messages/            # Message module
│   │   ├── websocket/           # WebSocket gateway
│   │   ├── app.module.ts
│   │   └── main.ts
│   ├── test/                    # Unit tests
├── docker-compose.yml           # (Optional) For MySQL and MongoDB
├── README.md
└── package.json
```

## Notes
- Use environment variables for sensitive data (e.g., database credentials, JWT secret).
- Ensure the application handles edge cases (e.g., user disconnects during a video call).
- Optimize WebRTC signaling for low latency.
- Keep the codebase simple but functional, focusing on the core requirements.

## Time Limit
- Complete the task within **8 hours**.
- Submit the GitHub repository link and any additional details (e.g., demo link) by the deadline.

Good luck! We look forward to reviewing your submission.
