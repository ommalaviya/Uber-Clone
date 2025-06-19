# Uber-Clone Project

## Overview
The Uber-Clone project is a ride-hailing application built using the MERN (MongoDB, Express.js, React.js, Node.js) stack. This project aims to replicate key features of the popular Uber app, including user and rider registration, ride searching, live location tracking, and more.

## Features
- **User and Rider Authentication**:
  - Login and Register as a user or rider.
  - JWT-based authentication.

- **Ride Searching**:
  - Search for rides based on destination and location.

- **Live Tracking**:
  - Real-time ride tracking using Google Maps API.
  - Live location updates for both users and riders.

- **Location Suggestions**:
  - Auto-suggestions for locations using Google Maps API.

- **Socket.io Integration**:
  - Real-time communication for ride updates and tracking.

## Technology Stack
- **Frontend**:
  - React.js
  - CSS for styling

- **Backend**:
  - Node.js with Express.js

- **Database**:
  - MongoDB

- **APIs and Libraries**:
  - Google Maps API for location services and live tracking.
  - Socket.io for real-time communication.

## Endpoints

### Authentication
1. **Register User**
   - **URL**: `/api/auth/register`
   - **Method**: POST
   - **Description**: Register a new user or rider.
   - **Payload**:
     ```json
     {
       "name": "string",
       "email": "string",
       "password": "string",
       "role": "user" | "rider"
     }
     ```

2. **Login**
   - **URL**: `/api/auth/login`
   - **Method**: POST
   - **Description**: Login as a user or rider.
   - **Payload**:
     ```json
     {
       "email": "string",
       "password": "string"
     }
     ```

### Ride Management
3. **Search Ride**
   - **URL**: `/api/rides/search`
   - **Method**: GET
   - **Description**: Search for rides based on location and destination.
   - **Query Parameters**:
     - `origin` (string): Starting location.
     - `destination` (string): Desired location.

4. **Live Tracking**
   - **URL**: `/api/rides/live-tracking`
   - **Method**: GET
   - **Description**: Get live tracking updates for the ride.

### Location Services
5. **Location Suggestions**
   - **URL**: `/api/locations/suggestions`
   - **Method**: GET
   - **Description**: Get location suggestions based on user input.
   - **Query Parameters**:
     - `input` (string): Partial location string for suggestions.

## Installation and Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/uber-clone.git
   ```

2. **Install Dependencies**:
   - Navigate to the project directory and install backend dependencies:
     ```bash
     cd uber-clone/backend
     npm install
     ```
   - Navigate to the frontend directory and install dependencies:
     ```bash
     cd ../frontend
     npm install
     ```

3. **Environment Variables**:
   - Create a `.env` file in the backend directory and add the following:
     ```env
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret
     GOOGLE_MAPS_API_KEY=your_google_maps_api_key
   ```

4. **Run the Application**:
   - Start the backend server:
     ```bash
     cd backend
     npm run dev
     ```
   - Start the frontend server:
     ```bash
     cd ../frontend
     npm start
     ```

## Usage
- Register as a user or rider.
- Search for rides and track them live.
- Experience real-time updates via socket communication.

## Acknowledgments
- Google Maps API for location services.
- Socket.io for real-time communication.







