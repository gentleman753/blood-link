# Blood-Link: MERN Stack Blood Bank Management System

## Project Overview
Blood-Link is a comprehensive MERN (MongoDB, Express.js, React, Node.js) stack application designed to manage blood bank operations efficiently. This project aims to streamline the process of blood donation, requests, and inventory management, connecting donors, hospitals, and organizations.

## Features
- **User Authentication**: Secure login and registration for donors, hospitals, and organizations.
- **Role-Based Access Control**: Different dashboards and functionalities based on user roles (Admin, Donor, Hospital, Organization).
- **Blood Inventory Management**: Track available blood units by type.
- **Donation Management**: Record and manage blood donations.
- **Request Management**: Hospitals and organizations can request blood units.
- **Analytics Dashboard**: Overview of blood inventory, donations, and requests for administrators.
- **Responsive UI**: Built with React for a dynamic and user-friendly experience.

## Technologies Used

### Backend (Server)
- **Node.js**: JavaScript runtime environment.
- **Express.js**: Web application framework for Node.js.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: ODM (Object Data Modeling) library for MongoDB and Node.js.
- **bcryptjs**: For hashing passwords.
- **jsonwebtoken**: For secure authentication (JWT).
- **morgan**: HTTP request logger middleware.
- **colors**: For colorful console output.
- **dotenv**: For managing environment variables.

### Frontend (Client)
- **React**: JavaScript library for building user interfaces.
- **Redux Toolkit**: For state management.
- **React Router DOM**: For navigation and routing.
- **Axios**: For making HTTP requests.
- **React Icons**: For various icons.
- **React Toastify**: For toast notifications.
- **Moment.js**: For parsing, validating, manipulating, and formatting dates.

### Development Tools
- **Nodemon**: Automatically restarts the Node.js server on file changes.
- **Concurrently**: Runs multiple commands concurrently (e.g., client and server).

## Installation and Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud-based like MongoDB Atlas)

### Steps

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/gentleman753/blood-link.git
    cd blood-link
    ```

2.  **Backend Setup:**
    ```bash
    npm install
    ```
    Create a `.env` file in the root directory and add your environment variables:
    ```
    MONGO_URL=your_mongodb_connection_string
    PORT=8080
    JWT_SECRET=your_jwt_secret_key
    ```

3.  **Frontend Setup:**
    ```bash
    cd client
    npm install
    ```
    Create a `.env` file in the `client` directory and add your environment variables:
    ```
    REACT_APP_API=http://localhost:8080/api/v1
    ```
    (Note: Adjust the API URL if your backend runs on a different port or domain.)

4.  **Run the application:**
    From the root directory, run:
    ```bash
    npm run dev
    ```
    This command will start both the backend server and the frontend development server concurrently.

## Project Structure

```
.
├── client/                 # React frontend application
│   ├── public/             # Public assets
│   ├── src/                # React source code
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Application pages (Auth, Dashboard, Admin, etc.)
│   │   ├── redux/          # Redux store and slices
│   │   ├── services/       # API service calls
│   │   └── styles/         # CSS stylesheets
│   └── package.json
├── config/                 # Backend configuration (e.g., DB connection)
├── controllers/            # Backend logic for routes
├── middlewares/            # Express middleware (auth, admin)
├── models/                 # Mongoose schemas
├── routes/                 # API routes
├── .env.example            # Example environment variables
├── package.json            # Backend dependencies and scripts
├── README.md               # Project documentation
└── server.js               # Main backend server file
```

## Deployment

### Backend Deployment
To deploy the backend, you can use platforms like Heroku, Vercel, or a custom VPS.

1.  **Environment Variables**: Ensure all necessary environment variables (`MONGO_URL`, `PORT`, `JWT_SECRET`) are configured in your deployment environment.
2.  **Build Process**: For production, you might want to build the client and serve it statically from the Express server, or deploy the client separately.

### Frontend Deployment
To deploy the React frontend, you can use platforms like Netlify, Vercel, or GitHub Pages.

1.  **Build the client application**:
    ```bash
    cd client
    npm run build
    ```
    This will create a `build` folder in the `client` directory with the optimized production build.
2.  **Serve the `build` folder**:
    -   If deploying separately, configure your hosting service to serve the contents of the `client/build` directory.
    -   If serving from the backend, you would typically copy the `client/build` contents to a `public` or `static` folder in your backend and configure Express to serve static files.

## Contribution
Contributions are welcome! Please feel free to fork the repository, create a new branch, and submit a pull request.

## License
This project is licensed under the ISC License.
