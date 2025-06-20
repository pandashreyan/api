📚 Book API

A simple RESTful API for managing books using Node.js, Express, and MongoDB.
Perfect for learning backend development through hands-on CRUD operations.

🚀 Features
📖 Create, Read, Update, Delete (CRUD) operations for books

🌐 RESTful API design principles

🗃️ MongoDB (local or Atlas) integration using Mongoose

⚙️ Configurable via .env file

🧪 Easily test endpoints with Postman or PowerShell

📋 Requirements
📦 Node.js v18 or higher

🗄️ MongoDB (local or MongoDB Atlas)

🔬 Postman or PowerShell for testing

⚙️ Setup Instructions
1. 📥 Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/book-api.git
cd book-api
2. 📦 Install Dependencies
bash
Copy
Edit
npm install
3. 🛠️ Create a .env File
In the root directory, create a .env file and add the following:

env
Copy
Edit
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
PORT=3000
⚠️ Replace <username>, <password>, <cluster>, and <database> with your actual MongoDB Atlas credentials.

4. ▶️ Start the Server
bash
Copy
Edit
npm start
📍 Server will run at: http://localhost:3000

📡 API Endpoints
Method	Endpoint	Description
POST	/api/books	Create a new book
GET	/api/books	Get all books
GET	/api/books/:id	Get a book by ID
PUT	/api/books/:id	Update a book by ID
DELETE	/api/books/:id	Delete a book by ID

🧪 PowerShell Testing Examples
✅ Create a Book
powershell
Copy
Edit
$book = @{
    title = "The Great Gatsby";
    author = "F. Scott Fitzgerald";
    publishedYear = 1925
} | ConvertTo-Json

Invoke-RestMethod -Uri "http://localhost:3000/api/books" -Method Post -Body $book -ContentType "application/json"
📖 Get All Books
powershell
Copy
Edit
Invoke-RestMethod -Uri "http://localhost:3000/api/books" -Method Get
📗 Get a Book by ID
powershell
Copy
Edit
$id = "REPLACE_WITH_BOOK_ID"
Invoke-RestMethod -Uri "http://localhost:3000/api/books/$id" -Method Get
✏️ Update a Book
powershell
Copy
Edit
$id = "REPLACE_WITH_BOOK_ID"
$update = @{ publishedYear = 2024 } | ConvertTo-Json

Invoke-RestMethod -Uri "http://localhost:3000/api/books/$id" -Method Put -Body $update -ContentType "application/json"
❌ Delete a Book
powershell
Copy
Edit
$id = "REPLACE_WITH_BOOK_ID"
Invoke-RestMethod -Uri "http://localhost:3000/api/books/$id" -Method Delete
🧰 Technologies Used
Node.js – JavaScript runtime

Express – Web framework for Node.js

MongoDB – NoSQL database

Mongoose – ODM for MongoDB

dotenv – Loads environment variables from .env

📁 Project Structure
bash
Copy
Edit
book-api/
│
├── models/
│   └── Book.js         # Mongoose schema
│
├── routes/
│   └── bookRoutes.js   # Route handlers
│
├── .env                # Environment variables
├── server.js           # Entry point of the app
├── package.json        # Project metadata & scripts
└── README.md           # Project documentation
📌 Notes
✅ Ensure your MongoDB Atlas cluster allows connections from your current IP address.

✅ Replace BOOK_ID in examples with a valid _id returned from the API.

✅ For local MongoDB setup, use the following instead in your .env file:

env
Copy
Edit
MONGODB_URI=mongodb://localhost:27017/bookdb
👨‍💻 Author
Shreyan Panda
🔗 GitHub: @pandashreyan

📄 License
This project is licensed under the MIT License.

⭐ Show Your Support
If you found this project helpful, please give it a ⭐ on GitHub!
Your feedback, contributions, and ideas are always welcome. 😊
