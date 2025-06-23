# 📚 Book API
This is a RESTful API for managing books, built with Node.js, Express, and MongoDB. The API provides endpoints for creating, reading, updating, and deleting book records.

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

```env
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
PORT=3000
```
⚠️ Replace with your MongoDB Atlas credentials.

For local MongoDB, use:

```env
MONGODB_URI=mongodb://localhost:27017/bookdb
```
4. ▶️ Start the Server
   
```bash
npm start
```
The API will be accessible at:
```
🔗 http://localhost:3000
```

📡 API Endpoints

Method	Endpoint	Description
POST	/api/books	Create a new book
GET	/api/books	Get all books
GET	/api/books/:id	Get a book by ID
PUT	/api/books/:id	Update a book by ID
DELETE	/api/books/:id	Delete a book by ID

🧪 PowerShell Testing Examples
✅ Create a Book
```powershell

$book = @{
    title = "1984";
    author = "George Orwell";
    publishedYear = 1949
} | ConvertTo-Json

Invoke-RestMethod -Uri "http://localhost:3000/api/books" -Method Post -Body $book -ContentType "application/json"
```
📖 Get All Books
```powershell
Invoke-RestMethod -Uri "http://localhost:3000/api/books" -Method Get
```
📗 Get a Book by ID
```powershell
$id = "REPLACE_WITH_BOOK_ID"
Invoke-RestMethod -Uri "http://localhost:3000/api/books/$id" -Method Get
```
✏️ Update a Book
```powershell

$id = "REPLACE_WITH_BOOK_ID"
$update = @{ publishedYear = 2024 } | ConvertTo-Json

Invoke-RestMethod -Uri "http://localhost:3000/api/books/$id" -Method Put -Body $update -ContentType "application/json"
```
❌ Delete a Book
```powershell

$id = "REPLACE_WITH_BOOK_ID"
Invoke-RestMethod -Uri "http://localhost:3000/api/books/$id" -Method Delete
```
🧰 Technologies Used:


### 🖥 Backend
- Node.js - JavaScript runtime environment
- Express.js - Web application framework
- MongoDB - NoSQL database
- Mongoose - MongoDB object modeling tool
### ✅ Testing
- Jest - JavaScript testing framework
- Supertest - HTTP assertions library for testing API endpoints
- MongoDB Memory Server - In-memory MongoDB server for testing

📁 Project Structure
```bash
api/
├── controllers/                 # Controller logic for book operations
│   └── bookController.js
├── models/                     # Mongoose schema definitions
│   └── Book.js
├── routes/                     # Express API route definitions
│   └── bookRoutes.js
├── tests/                      # Test suites
│   ├── Apis/                   # API tests using mocks/stubs
│   │   └── bookApi.test.js
│   ├── integration/            # Tests involving actual DB connections
│   │   └── bookApi.test.js
│   └── unit/                   # Unit tests for isolated controller functions
│       └── bookController.test.js
├── .env                        # Environment variables (ignored by Git)
├── server.js                   # Main entry point, Express server setup
├── jest.config.js              # Jest testing configuration
└── package.json                # Project metadata and dependencies

```

📡 API Endpoints

| Method | Endpoint         | Description         |
| ------ | ---------------- | ------------------- |
| POST   | `/api/books`     | Create a new book   |
| GET    | `/api/books`     | Get all books       |
| GET    | `/api/books/:id` | Get a book by ID    |
| PUT    | `/api/books/:id` | Update a book by ID |
| DELETE | `/api/books/:id` | Delete a book by ID |

## Setup and Installation
1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a .env file in the root directory with the following variables:
   ```
   MONGODB_URI=mongodb://
   localhost:27017/bookdb
   PORT=3000
   ```
   Note: Replace with your MongoDB connection string if using MongoDB Atlas.
## Running the Application
Start the server:

```
npm start
```
The API will be available at http://localhost:3000 .

## Running Tests
Run all tests with coverage report:

```
npm test
```
### Testing Strategy
The project implements a comprehensive testing approach:

🔹 Unit tests: Validate controller logic in isolation
🔸 Integration tests: Verify real DB interactions
🟢 API tests: Mocked endpoints with expected responses


## Test Coverage
The project has excellent test coverage:
<img src="https://github.com/user-attachments/assets/366333ee-b923-4458-a062-7d52d6a40407" alt="Test Coverage" style="width:100%; max-width:900px;" />



- 100% of branches and functions are covered
- 87.23% of lines are covered
- 88% of statements are covered
- The only uncovered lines are in the controller (lines 8, 30-31, 41, 51, 61), which are likely error handling or edge cases.

## Book Model
The Book model includes the following fields:
```
  {
  title: String,        // required
  author: String,       // required
  publishedYear: Number // required
}
```
## Development
This project uses the following development tools:

- Jest for testing
- Supertest for API testing
- MongoDB Memory Server for in-memory database testing
  
🔒 Security Note
Make sure to add sensitive files to your .gitignore:

```bash
.env
node_modules/
Never commit your actual MongoDB credentials to GitHub.
```

👨‍💻 Author
Shreyan Panda              🔗 GitHub: @pandashreyan

📄 License
This project is licensed under the MIT License.
See the LICENSE file for more details.

⭐ Show Your Support
If you found this project helpful:

```
Give it a ⭐ on GitHub
Share it with others
Feel free to fork and contribute!
```

Your feedback, ideas, and pull requests are always welcome. 😊

   
