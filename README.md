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
- [MongoDB](https://www.mongodb.com/) (local or Atlas cloud instance)
- Postman or PowerShell for testing endpoints

---

## ⚙️ Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/book-api.git
cd book-api
2. Install dependencies
bash
Copy
Edit
npm install
3. Create a .env file in the project root
env
Copy
Edit
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
PORT=3000
⚠️ Important: Replace <username>, <password>, <cluster>, and <database> with your actual MongoDB credentials.

4. Start the server
bash
Copy
Edit
npm start
The API will be available at:
http://localhost:3000

📡 API Endpoints
Method	Endpoint	Description
POST	/api/books	Create a new book
GET	/api/books	Get all books
GET	/api/books/:id	Get a single book
PUT	/api/books/:id	Update a book by ID
DELETE	/api/books/:id	Delete a book by ID

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
Node.js – JavaScript runtime

Express – Backend web framework

MongoDB – NoSQL document database

Mongoose – MongoDB ODM (Object Data Modeling)

dotenv – Load environment variables

📁 Project Structure
bash
Copy
Edit
book-api/
│
├── models/
│   └── Book.js         # Mongoose book schema
│
├── routes/
│   └── bookRoutes.js   # All book-related API routes
│
├── .env                # Environment variables
├── server.js           # Main entry point
├── package.json        # Project metadata and scripts
└── README.md           # Project documentation
📌 Notes
✅ Ensure MongoDB Atlas is accessible and the network access allows your IP.

✅ Replace "BOOK_ID" in examples with a valid ObjectId returned from POST requests.

✅ For local MongoDB, replace MONGODB_URI with:

bash
Copy
Edit
mongodb://localhost:27017/bookdb
👨‍💻 Author
Shreyan Panda
📎 GitHub: @pandashreyan

📄 License
This project is licensed under the MIT License.

⭐️ Show Your Support
If you like this project, please give it a ⭐ on GitHub!
Contributions and feedback are always welcome.

yaml
Copy
Edit

---

Would you also like me to generate:
- `LICENSE` file (MIT)?
- `.gitignore` file?
- Sample API testing collection for Postman?








