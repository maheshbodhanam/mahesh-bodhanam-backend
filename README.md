# 📬 Contact Form Backend 

This is a simple Node.js backend API for handling contact form submissions, built with Express.js, MongoDB (Mongoose), and CORS.

### 📁 Project Structure

```
│
├── server.js               # Entry point for the server
├── .env                   # Environment variables (e.g., MongoDB URI, Port)
├── models/
│   └── Contact.js         # Mongoose schema for contact form
├── routes/
│   └── contact.js         # API route to handle contact form submission
├── package.json           # Node dependencies and scripts


```
### 🛠️ Tech Stack
Node.js

Express.js

MongoDB (with Mongoose)

dotenv

CORS

## 🚀 How to Run the Project Locally
### 1. Clone the repository
```
git clone https://github.com/yourusername/contact-form-backend.git
cd contact-form-backend
```
### 2. Install dependencies
```
npm install
```
### 3. Setup Environment Variables

Create a .env file in the root of the project and add the following:
```
PORT=5000
MONGO_URI=your_mongodb_connection_string
```
### Example MongoDB URI:
MONGO_URI=mongodb+srv://mahesh:yourPassword@cluster0.mongodb.net/contactForm?retryWrites=true&w=majority

### ⚠️ Replace your_mongodb_connection_string with your actual MongoDB URI.

### 4. Start the Server
```
node server.js
```
### You should see:
MongoDB connected
Server running on port 5000


### 📌 API Endpoint
POST /api/contact
```
Request Body:
{
  "name": "John Doe",
  "email": "john@example.com",
  "message": "Hello, I want to get in touch!"
}
Success Response:
{
  "success": true,
  "message": "Message sent successfully."
}
Error Responses:
If any field is missing:
{
  "error": "All fields are required."
}
If server fails:
{
  "error": "Server error. Please try again later."
}
```
## 🧱 Architecture & Approach
**MVC Pattern:** The project follows a minimal MVC-like structure.

**Model:** Contact.js defines a Mongoose schema to store name, email, and message.

**Routes:** contact.js handles the POST request and data validation.

**Server:** server.js sets up middleware, connects to MongoDB, and integrates routes.

### Security & Clean Code:

Sensitive data like MongoDB URI is stored in .env.

CORS is enabled to allow frontend connections.

JSON parsing middleware is used to handle incoming form data.

### 🧪 Testing the API
You can use Postman or cURL to test the /api/contact endpoint by sending a POST request with name, email, and message in the body.
