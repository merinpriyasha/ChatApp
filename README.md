# Chat Application

A real-time chat application built with Node.js, Express, MongoDB, Socket.IO, and JWT authentication. Users can sign up, log in, and chat with other online users in real-time.

## 📌 Features

* User registration and login with JWT authentication.
* Passwords are securely hashed using bcrypt.
* Real-time messaging with Socket.IO.
* Users can see online users in the sidebar.
* Each user can only see their own messages.
* Automatic profile picture generation based on gender.
* REST API for fetching users and messages.

## 🛠️ Technologies Used

* Backend: Node.js, Express
* Database: MongoDB (Mongoose)
* Authentication: JWT, bcrypt
* Real-time Communication: Socket.IO
* Frontend: React.js

## 💻 Setup & Installation
1. Clone the repository:
   ```
   git clone https://github.com/merinpriyasha/ChatApp.git
   cd ChatApp
   
2. Install dependencies:
   ```
   npm install
   
3. Add environment variables:
Create a .env file in the root directory and add the following:

    ```
    PORT=5000
    MONGO_DB_URI=<Your MongoDB URI>
    JWT_SECRET=<Your JWT Secret>
    NODE_ENV=development

    ```

4. Start the server:
    ```
    npm run dev
    ```
## API Endpoints

### Authentication

| Method	    | Endpoint	      | Description	Body                                                              |
|-------------|-----------------|-------------------------------------------------------------------------------|
| POST	      | /auth/signup	  | Register a new user	{ fullName, username, password, confirmPassword, gender } |
| POST	      | /auth/login	    | Login user and generate JWT	{ username, password }                            |
| POST	      | /auth/logout	  | Logout user and clear cookie	None                                            |

### Users
| Method	    | Endpoint	      | Description	Body                            |
|-------------|-----------------|---------------------------------------------|
| GET	        | /users/sidebar  |	Get all users except logged-in user         |

### Messages
| Method	    | Endpoint	      | Description	Body                                                 |
|-------------|-----------------|------------------------------------------------------------------|
| POST	      | /messages/:id	  | Send message to a user	{ message }                              |
| GET	        | /messages/:id	  | Get all messages between logged-in user and another user	None   |

## 🖼 Screenshots

<img width="1417" height="863" alt="loginpage-chatapp" src="https://github.com/user-attachments/assets/b98914bf-16d0-4bb7-997d-071bb89e50fd" />

<img width="1101" height="785" alt="chat between jane" src="https://github.com/user-attachments/assets/35a174a5-d1a3-4be0-8dd8-276cf117c1da" />


<img width="1176" height="760" alt="chat between sam" src="https://github.com/user-attachments/assets/453366d3-1a3b-4267-9df1-3935effc6023" />


###  live web app link
https://chat-app-prod-xa66.onrender.com

username = bobdoe
password=123456

username=janedoe
password=123456

username=samclient
password=123456
