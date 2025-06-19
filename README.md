Overview
The Uber-Clone project is a ride-hailing application built using the MERN (MongoDB, Express.js, React.js, Node.js) stack. This project aims to replicate key features of the popular Uber app, including user and rider registration, ride searching, live location tracking, and more.
Features
User and Rider Authentication:

Login and Register as a user or rider.
JWT-based authentication.
Ride Searching:

Search for rides based on destination and location.
Live Tracking:

Real-time ride tracking using Google Maps API.
Live location updates for both users and riders.
Location Suggestions:

Auto-suggestions for locations using Google Maps API.
Socket.io Integration:

Real-time communication for ride updates and tracking.
Technology Stack
Frontend:

React.js
CSS for styling
Backend:

Node.js with Express.js
Database:

MongoDB
APIs and Libraries:

Google Maps API for location services and live tracking.
Socket.io for real-time communication.
Endpoints
Authentication
Register User

URL: /api/auth/register
Method: POST
Description: Register a new user or rider.
Payload:
{
  "name": "string",
  "email": "string",
  "password": "string",
  "role": "user" | "rider"
}
Login

URL: /api/auth/login
Method: POST
Description: Login as a user or rider.
Payload:
{
  "email": "string",
  "password": "string"
}
Ride Management
Search Ride

URL: /api/rides/search
Method: GET
Description: Search for rides based on location and destination.
Query Parameters:
origin (string): Starting location.
destination (string): Desired location.
Live Tracking

URL: /api/rides/live-tracking
Method: GET
Description: Get live tracking updates for the ride.
Location Services
Location Suggestions
URL: /api/locations/suggestions
Method: GET
Description: Get location suggestions based on user input.
Query Parameters:
input (string): Partial location string for suggestions.
Installation and Setup
Clone the Repository:

git clone https://github.com/your-username/uber-clone.git
Install Dependencies:

Navigate to the project directory and install backend dependencies:
cd uber-clone/backend
npm install
Navigate to the frontend directory and install dependencies:
cd ../frontend
npm install
Environment Variables:

Create a .env file in the backend directory and add the following:
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GOOGLE_MAPS_API_KEY=your_google_maps_api_key

Run the Application:

Start the backend server:
cd backend
npm run dev
Start the frontend server:
cd ../frontend
npm start
Usage
Register as a user or rider.
Search for rides and track them live.
Experience real-time updates via socket communication.
Acknowledgments
Google Maps API for location services.
Socket.io for real-time communication.
