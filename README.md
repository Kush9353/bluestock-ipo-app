# bluestock-ipo-app
Bluestock IPO Web App & REST API
This project is a full-stack application designed to manage and display Initial Public Offering (IPO) data. It was developed during an internship at Bluestock Fintech. The application supports user registration, login, viewing IPO listings and their details, and applying for IPOs. 

Key Features

User Management: Functionality for user registration and login. 
IPO Listings: View a list of all available Initial Public Offerings. 
Detailed IPO View: See more information for a specific IPO. 
IPO Application: A planned feature to allow users to apply for IPOs. 



Tech Stack
The project is divided into a frontend single-page application and a backend REST API. 

Frontend

Language: JavaScript 
Framework: React (Create React App) 
Libraries:
Axios for HTTP requests 
Tailwind CSS for styling 
React Router DOM for navigation 

Backend
Language: JavaScript 
Framework: Node.js with Express 
Libraries:
Mongoose for MongoDB interaction 
BcryptJS for password hashing 
Dotenv for environment variable management 
CORS for handling Cross-Origin Resource Sharing 

Database
Primary Database: MongoDB, hosted on MongoDB Atlas. 
Architecture
Frontend: A Single Page Application built with React. 
Backend: A REST API developed with Node.js and Express, following an MVC-style pattern. 

Data Flow: The data flows from the React client to the Express API, which then interacts with the MongoDB Atlas database. The API sends the response back to the client. 

Getting Started
Prerequisites
Node.js and npm

Git

Installation & Setup
As per Bluestock's IP policy, public deployment of this project is not permitted. It is intended for local development only. 


Clone the Repositories:
Clone both the frontend and backend repositories. 

Backend Setup:

Bash

cd backend
npm install
cp .env.example .env
# Add your MongoDB connection string and other environment variables to the .env file
node app.js
The backend API will be accessible at 

http://localhost:5000. 

Frontend Setup:

Bash

cd frontend
npm install
npm start
The frontend application will be running at 

http://localhost:3000. 

API Endpoints
The following are the available endpoints for the REST API:

Endpoint	Method	Description	Parameters	Response
/api/auth/register	POST	
Register a new user. 

name, email, password 

JSON message 

/api/auth/login	POST	
Log in a user. 


email, password 

JSON message / token 


/api/ipos	GET	
Retrieve all IPOs. 

None 

List of IPO objects 

/api/ipos/:id	GET	
Get details for a specific IPO. 

URL parameter: 

id 

A single IPO object 

/api/applications	POST		
(Planned) Apply for an IPO. 

ipold, quantity 

Application response 


Export to Sheets
Security

Password Hashing: User passwords are securely hashed using bcryptjs. 

Input Validation: Input is validated at the controller level. 

Environment Variables: Sensitive data like API keys and database URIs are managed using .env files. 


CORS: The backend is configured to only allow requests from the frontend's origin. 

Future Improvements
The following features and enhancements are planned for future development:


Authentication: Implement JWT-based login and user sessions. 


Admin Panel: Create an admin dashboard for managing IPOs. 


Application Tracking: Full implementation of IPO application submission and status tracking. 

Real-time Updates: Use WebSockets for real-time data updates.


Testing: Add unit and integration tests using Jest and Supertest. 



Containerization: Dockerize the application for easier deployment and scaling. 
