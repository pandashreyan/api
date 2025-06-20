# 📚 Book API

A simple RESTful API for managing books using **Node.js**, **Express**, and **MongoDB**.  
This API allows users to perform CRUD operations on a collection of books and is ideal for learning backend development with Express and MongoDB.

---

## 🚀 Features

- 📖 Create, Read, Update, Delete (CRUD) books
- 🌐 RESTful API design
- 🗃️ MongoDB integration (local or Atlas)
- ⚙️ Environment-based configuration using `.env`
- 🧪 Easy testing with Postman or PowerShell

---

## 📋 Requirements

- [Node.js](https://nodejs.org/) v18+
- [MongoDB](https://www.mongodb.com/) (local or cloud via MongoDB Atlas)
- Postman or PowerShell for testing endpoints

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/book-api.git
cd book-api
2. Install Dependencies
bash
Copy
Edit
npm install
3. Create .env File in the Project Root
env
Copy
Edit
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
PORT=3000
⚠️ Important: Replace <username>, <password>, <cluster>, and <database> with your actual MongoDB Atlas credentials.

4. Start the Server
bash
Copy
Edit
npm start
Server will be running at: http://localhost:3000

📡 API Endpoints
Method	Endpoint	Description
POST	/api/books	Create a new book
GET	/api/books	Get all books
GET	/api/books/:id	Get a single book
PUT	/api/books/:id	Update a book
DELETE	/api/books/:id	Delete a book

🧪 PowerShell Usage Examples
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
Node.js – JavaScript runtime environment

Express – Web framework for Node.js

MongoDB – NoSQL document database

Mongoose – MongoDB ODM for Node.js

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
│   └── bookRoutes.js   # Route definitions
│
├── .env                # Environment config
├── server.js           # Entry point
├── package.json        # Dependencies & scripts
└── README.md           # Project documentation
📌 Notes
✅ Make sure MongoDB Atlas allows connections from your IP.

✅ Replace BOOK_ID with a valid ObjectId returned from the create API.

✅ For local MongoDB, use:

bash
Copy
Edit
MONGODB_URI=mongodb://localhost:27017/bookdb
👨‍💻 Author
Shreyan Panda
GitHub: @pandashreyan

📄 License
This project is licensed under the MIT License.

⭐ Show Your Support
If you like this project, please give it a ⭐ on GitHub!
Contributions and feedback are welcome!

yaml
Copy
Edit

---

Would you like me to generate the `LICENSE` and `.gitignore` files for this project as well?


