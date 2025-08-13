LinkedIn Clone
A full-stack web application designed to mimic core functionalities of the professional networking platform, LinkedIn. Users can create profiles, connect with other professionals, and create and interact with posts.

Features
User Authentication: Secure user registration, login, and authentication using JSON Web Tokens (JWT).

Profile Management: Users can create and update their professional profiles.

Posting: Create and share text-based posts, with support for image uploads.

Real-time Interactions: The application uses WebSockets (likely Socket.IO) to handle real-time user connections, which can be extended for features like live notifications or chat.

Data Storage: Uses a MongoDB database to store user and post information.

Cloud Storage: Integrates with Cloudinary for handling and storing image uploads.

Technologies Used
Frontend
React: For building the user interface.

Tailwind CSS: For modern and responsive styling.

Backend
Node.js & Express: The backend server framework.

MongoDB & Mongoose: The NoSQL database and its object data modeling (ODM) library.

JSON Web Tokens (JWT): For secure user authentication.

bcrypt.js: For hashing user passwords.

Cloudinary: For image storage and management.

Socket.IO: For enabling real-time communication.

Getting Started
Follow these steps to set up the project locally.

Prerequisites
Node.js (v14 or higher)

npm or yarn

MongoDB Atlas account (or a local MongoDB instance)

Cloudinary account

Installation
Clone the repository:

git clone https://github.com/Dev-Nitesh-Yadav/Linkedin
cd <your-repo-directory>

Install dependencies for the backend:

cd backend
npm install

Install dependencies for the frontend:

cd ../frontend
npm install

Configuration
Create a .env file in the backend directory.
Copy the contents of the .env.example (if one exists) or create a new one with the following keys and your credentials:

PORT=5000
MONGO_URI=mongodb+srv://<your-username>:<your-password>@<your-cluster>.mongodb.net/?retryWrites=true&w=majority
JWT_SECRET=your_super_secret_jwt_key_here
CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret

MONGO_URI: Get this from your MongoDB Atlas dashboard.

JWT_SECRET: Generate a long, random string.

Cloudinary Credentials: Find these on your Cloudinary dashboard.

Seed the Database (Optional but Recommended)
If you want to populate your database with some initial mock data for testing, you can use the seeding script.

node backend/scripts/seed.js

Running the Application
Start the backend server:

cd backend
npm run dev

The server will run on the port specified in your .env file (e.g., http://localhost:5000).

Start the frontend development server:

cd ../frontend
npm run dev

The frontend will open in your browser, typically at http://localhost:3000.

Troubleshooting
"User disconnected: undefined" error: This typically indicates a problem with the WebSocket (Socket.IO) connection. Check your CORS settings in the backend and ensure the frontend is connecting to the correct URL.

Post not working: Look for errors in your browser's developer console and your server's terminal. Issues are often related to incorrect API endpoints, authentication problems, or file upload logic.

Database Connection: Ensure your MONGO_URI is correct and your IP address is whitelisted in your MongoDB Atlas cluster settings.
