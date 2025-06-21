# Day2Task
Day 2 Task for Keploy API Fellowship

# 🛒 Product API Server – RESTful CRUD API with MongoDB

This project is a simple **Node.js + Express.js** server that provides a **custom RESTful API** for managing product data stored in a **MongoDB Atlas database**. It supports full **CRUD operations** via HTTP methods.

---

## 📌 Task Requirement Checklist ✅

| Requirement                              | Status  |
|------------------------------------------|---------|
| 🔧 Custom API with 4+ endpoints          | ✅ Done |
| 🗃️ Integrated with a real database       | ✅ Done |
| 💬 Supports Create, Read, Update, Delete | ✅ Done |
| 🧪 API tested via Insomnia               | ✅ Done |
| 📝 Documentation for APIs                | ✅ Done |
| 📂 GitHub-ready project with README.md   | ✅ Done |

---

## 🚀 Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB Atlas**
- **Mongoose (ODM)**
- **dotenv** for environment variables

---

## 📁 Project Structure
├── models/
│ └── product.model.js # Product schema
├── server.js # Main server file
├── .env # Environment variables (not committed)
├── package.json
└── README.md


---

## ⚙️ Environment Variables

Create a `.env` file in your project root:

```env
PORT=3000
MONGO_URI=mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/myapidata?retryWrites=true&w=majority&appName=Cluster0
```

## 🛠️ Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 3. Create .env file
Follow the .env.example file and add your MongoDB connection string.

### 4. Run the server
```bash
npm run dev   # if using nodemon
# or
node server.js
```

## 🌐 API Endpoints & Documentation

#### All routes are prefixed with /api.

### ➕ Create a Product
#### POST /api/products

📨 Request Body
```json
{
  "name": "Wireless Mouse",
  "quantity": 10,
  "price": 799.99,
  "image": "https://example.com/mouse.jpg"
}
```

📤 Response
```json
{
  "_id": "60f2...",
  "name": "Wireless Mouse",
  "quantity": 10,
  "price": 799.99,
  "image": "https://...",
  "createdAt": "...",
  "updatedAt": "..."
}
```
### 📥 Get All Products
#### GET /api/products

Returns a list of all stored products.

📤 Response
```json
[
  {
    "_id": "60f2...",
    "name": "Wireless Mouse",
    "quantity": 10,
    "price": 799.99
  },
  {
    "_id": "60f3...",
    "name": "Keyboard",
    "quantity": 5,
    "price": 1299.00
  }
]
```

### 🔍 Get Product by ID
#### GET /api/product/:id

Returns a single product by its MongoDB ID.

### ♻️ Update Product by ID
#### PUT /api/product/:id

Update one or more product fields.

📨 Request Body
```json
{
  "price": 699.99,
  "quantity": 5
}
```

### ❌ Delete Product by ID
#### DELETE /api/product/:id

Deletes a product by its ID.

📤 Response
```json
{
  "message": "Product deleted successfully !"
}
```




