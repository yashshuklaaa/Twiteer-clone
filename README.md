Backend Completion Tech Stack
This project is a backend implementation for a social media-like application, providing functionalities such as user authentication, post interactions (like, unlike, comment), and social interactions (follow, unfollow). The tech stack includes Node.js with Express for the server, MongoDB with Mongoose for the database, and several other libraries for various functionalities.

Tech Stack
bcryptjs: ^2.4.3
cloudinary: ^2.2.0
cookie-parser: ^1.4.6
cors: ^2.8.5
dotenv: ^16.4.5
express: ^4.19.2
jsonwebtoken: ^9.0.2
mongoose: ^8.3.4
Development Dependencies
nodemon: ^3.1.0
Features
User Authentication
Sign Up: Register a new user with hashed passwords using bcryptjs.
Sign In: Authenticate a user and issue a JSON Web Token (JWT) for session management.
Post Interactions
Like: Allow users to like a post.
Unlike: Allow users to unlike a post.
Comment: Allow users to comment on a post.
Social Interactions
Follow: Allow users to follow other users.
Unfollow: Allow users to unfollow other users.
Getting Started
Prerequisites
Node.js (>= 12.x)
MongoDB
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yashshuklaaa/Twiteer-clone
cd your-repository
Install dependencies:

bash
Copy code
npm install
Set up environment variables:

Create a .env file in the root directory and add the following variables:

plaintext
Copy code
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
Running the Server
Start the server in development mode using nodemon:

bash
Copy code
npm run dev
API Endpoints
Auth
POST /api/auth/signup

Registers a new user.
Request body: { username, email, password }
POST /api/auth/signin

Authenticates a user and returns a JWT.
Request body: { email, password }
Posts
POST /api/posts

Creates a new post.
Request body: { title, content, imageUrl }
Protected route (requires JWT).
POST /api/posts/
/like

Likes a post.
Protected route (requires JWT).
POST /api/posts/
/unlike

Unlikes a post.
Protected route (requires JWT).
POST /api/posts/
/comment

Comments on a post.
Request body: { comment }
Protected route (requires JWT).
Users
POST /api/users/
/follow

Follows a user.
Protected route (requires JWT).
POST /api/users/
/unfollow

Unfollows a user.
Protected route (requires JWT).
Libraries and Their Roles
bcryptjs: Used for hashing user passwords before saving them to the database.
cloudinary: Handles image uploads and management.
cookie-parser: Parses cookies attached to client requests.
cors: Enables Cross-Origin Resource Sharing.
dotenv: Loads environment variables from a .env file into process.env.
express: Framework for building the RESTful API.
jsonwebtoken: Used for creating and verifying JSON Web Tokens (JWTs) for user authentication.
mongoose: ODM (Object Data Modeling) library for MongoDB, providing a straightforward schema-based solution to model application data.
nodemon: Development tool that automatically restarts the server upon file changes.