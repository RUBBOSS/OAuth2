# OAouth

## Description

OAouth is a web application that allows users to share secrets anonymously. It includes features for user authentication via local credentials and Google OAuth. The application uses Express, Passport.js, and PostgreSQL to manage users and secrets.

## Features

- **User Authentication**: Supports login and registration with local credentials and Google OAuth.
- **Anonymous Secrets Sharing**: Allows authenticated users to submit and view secrets anonymously.
- **Session Management**: Manages user sessions securely with Express Session.

## Technologies Used

- **Frontend**: HTML, CSS, Bootstrap
- **Backend**: Node.js, Express
- **Database**: PostgreSQL
- **Authentication**: Passport.js (Local and Google OAuth strategies)
- **Hashing**: bcrypt

## Getting Started

### Prerequisites

- Node.js
- PostgreSQL
- Google Developer Account for OAuth credentials

### Installation

1. **Clone the repository**

    ```bash
    git clone https://github.com/RUBBOSS/OAouth.git
    cd <repository-directory>
    ```

2. **Install dependencies**

    ```bash
    npm install
    ```

3. **Set up the PostgreSQL database**

    Create a database named `secrets` and set up the `users` table.

    Example SQL queries:

    ```sql
    CREATE TABLE users (
        email VARCHAR(255) UNIQUE NOT NULL,
        password VARCHAR(255) NOT NULL
    );
    ```

4. **Configure environment variables**

    Create a `.env` file in the root directory of your project with the following content:

    ```dotenv
    GOOGLE_CLIENT_ID="your-google-client-id"
    GOOGLE_CLIENT_SECRET="your-google-client-secret"
    SESSION_SECRET="your-session-secret"
    PG_USER="your-postgres-username"
    PG_HOST="localhost"
    PG_DATABASE="secrets"
    PG_PASSWORD="your-postgres-password"
    PG_PORT="5432"
    ```

5. **Start the server**

    ```bash
    npm start
    ```

    The server will run at `http://localhost:3000`.

## Usage

- **Home Page**: Go to `http://localhost:3000` to access the main page.
- **Login**: Navigate to `http://localhost:3000/login` to log in using your email and password or Google OAuth.
- **Register**: Go to `http://localhost:3000/register` to create a new account.
- **Secrets**: Once logged in, visit `http://localhost:3000/secrets` to view and share secrets.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions for improvements or bug fixes.
