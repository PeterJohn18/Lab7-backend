# Lab7 Backend - Authentication API

This is the backend component of the Lab7 full-stack authentication system, built with Node.js, Express, and MySQL.

## Live Links
* **Frontend Application:** https://lab7-peterjohn18.onrender.com
* **Backend API (Swagger):** https://lab7-backend-peterjohn18.onrender.com/api-docs
* **Frontend Repository:** https://github.com/PeterJohn18/lab7

## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/PeterJohn18/Lab7-backend.git
   cd Lab7-backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory with the following variables:
   ```
   DATABASE_URL=your_mysql_connection_string
   JWT_SECRET=your_jwt_secret_key
   EMAIL_FROM=your_email@example.com
   SMTP_HOST=smtp.ethereal.email
   SMTP_PORT=587
   SMTP_USER=your_ethereal_user
   SMTP_PASS=your_ethereal_pass
   ```
4. Run the server:
   ```bash
   npm start
   ```
   The API will be available at `http://localhost:4000` and Swagger docs at `http://localhost:4000/api-docs`.

## Production Configuration
- **Database**: Connects to a remote MySQL instance using the `DATABASE_URL` environment variable.
- **Emails**: Uses `ethereal.email` for testing verification and reset emails. Check server console logs for the Ethereal message links.
- **Security**: JWT secrets and database passwords are **never hardcoded**. All sensitive values are handled via environment variables.
- **CORS**: Set the `CORS_ORIGIN` environment variable to the URL of your deployed Angular frontend.
