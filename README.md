# Social Media Backend

This project is a backend implementation for a social media-like application, providing functionalities such as user authentication, post interactions (like, unlike, comment), and social interactions (follow, unfollow).

## Tech Stack

- **bcryptjs**: ^2.4.3
- **cloudinary**: ^2.2.0
- **cookie-parser**: ^1.4.6
- **cors**: ^2.8.5
- **dotenv**: ^16.4.5
- **express**: ^4.19.2
- **jsonwebtoken**: ^9.0.2
- **mongoose**: ^8.3.4

### Development Dependencies

- **nodemon**: ^3.1.0

## Features

### User Authentication

- **Sign Up**: Register a new user with hashed passwords using `bcryptjs`.
- **Sign In**: Authenticate a user and issue a JSON Web Token (JWT) for session management.

### Post Interactions

- **Like**: Allow users to like a post.
- **Unlike**: Allow users to unlike a post.
- **Comment**: Allow users to comment on a post.

### Social Interactions

- **Follow**: Allow users to follow other users.
- **Unfollow**: Allow users to unfollow other users.

## Getting Started

### Prerequisites

- Node.js (>= 12.x)
- MongoDB

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/your-repository.git
   cd your-repository
