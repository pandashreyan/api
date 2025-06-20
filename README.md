# 📚 Book API

A RESTful API for managing books using Node.js, Express, and MongoDB

## 🚀 Features
- CRUD operations for books
- RESTful API endpoints
- MongoDB integration with Mongoose
- Environment configuration
- PowerShell/Postman test examples

## 📋 Requirements
- Node.js v18+
- MongoDB Atlas account or local MongoDB
- Postman/PowerShell for testing

## ⚙️ Setup

1. Clone repository:
```bash
git clone https://github.com/your-username/book-api.git
cd book-api
```
2. 📦 Install Dependencies
```bash
npm install
```
3. 🛠️ Configure Environment Variables
Create a .env file in the root directory and add:

env
Copy
Edit
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
PORT=3000
⚠️ Replace <username>, <password>, <cluster>, and <database> with your MongoDB Atlas credentials.

For local MongoDB, use:

env
Copy
Edit
MONGODB_URI=mongodb://localhost:27017/bookdb
4. ▶️ Start the Server
bash
Copy
Edit
npm start
The API will be accessible at:
🔗 http://localhost:3000

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
    title = "1984";
    author = "George Orwell";
    publishedYear = 1949
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

Express.js – Lightweight web framework

MongoDB – NoSQL database

Mongoose – ODM for MongoDB

dotenv – Load environment variables from .env

📁 Project Structure
bash
Copy
Edit
book-api/
│
├── models/
│   └── Book.js           # Mongoose schema
│
├── routes/
│   └── bookRoutes.js     # Express routes for books
│
├── .env                  # Environment variables (ignored in git)
├── server.js             # Entry point of the application
├── package.json          # Project metadata & dependencies
└── README.md             # Project documentation
🔒 Security Note
Make sure to add sensitive files to your .gitignore:

bash
Copy
Edit
.env
node_modules/
Never commit your actual MongoDB credentials to GitHub.

👨‍💻 Author
Shreyan Panda
🔗 GitHub: @pandashreyan

📄 License
This project is licensed under the MIT License.
See the LICENSE file for more details.

⭐ Show Your Support
If you found this project helpful:

Give it a ⭐ on GitHub

Share it with others

Feel free to fork and contribute!

Your feedback, ideas, and pull requests are always welcome. 😊

   
