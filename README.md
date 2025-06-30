# 🔁 LooperAI

**LooperAI** is a full-stack application that allows users to track their financial transactions through an intuitive and beautifully designed dashboard. The app features advanced filtering, user authentication, export functionality, and visual analytics to help users better understand their spending habits.

---

## 📸 Preview

![Dashboard Preview](https://github.com/Akhilesh-Talekar/looperai/assets/preview.png) <!-- Replace with real image link -->

---

## ✨ Features

- 🔐 Secure user sign in / sign up page
- 📊 Interactive dashboard with:
  - Total expense
  - Balance
  - Revenue
  - Expense vs Revenue graph (monthly)
- 📁 Paginated table with advanced filters
- 📈 Graphical visualization using Recharts
- ⬇ Export transactions to Excel/CSV
- ⚡ Responsive & beautiful UI using Aceternity UI

---

## 🗂 Project Structure
looperai/
├── backend/
│ ├── index.js
│ ├── .env
│ └── ...
└── frontend/
├── src/
├── .env
└── ...


---

## 🚀 Getting Started

### 🔁 Clone the repository

```bash
git clone https://github.com/Akhilesh-Talekar/looperai.git
cd looperai
```

###🔧 Backend Setup

1. Navigate to the backend folder:

```bash
cd backend
```

2. Install dependencies:

```bash
npm install
```

3. Create a .env file in the backend root and add:

```ini
MONGO_URL=<your_mongo_connection_string>
TOKEN_KEY=<your_jwt_secret_key>
```
4. Run the backend server:

```bash
nodemon index.js
```

## 🌐 Frontend Setup

1. Go to the frontend directory:

```bash
cd ../frontend
```

2. Install dependencies:

```bash
npm install
```

3. Create a .env file in the frontend root and add:

```ini
VITE_BACKEND_URL=<Your Backend URL HERE>
```

4. Update backend CORS configuration to allow frontend access:
   In backend/index.js, modify the CORS settings:

   ```bash
   app.use(
    cors({
    origin: [<Your Frontend URL Here>], // Add all frontend URLs explicitly
    methods: ["GET", "POST", "PUT", "DELETE"],
    credentials: true,
    allowedHeaders: [
      "Content-Type",
      "Authorization",
      "X-Requested-With",
      "Accept",
    ],
    })
    );
   ```

5. Start the frontend server:
   ```bash
   npm run dev
   ```

6. Open the URL shown in your terminal (e.g., http://localhost:5173)

## 📝 Signup Note ⚠
⚠️ While signing up, please use one of the following userIds:

user_001

user_002

user_003

These IDs match the pre-seeded transaction data in the database. You can enter any email and password. For example:

```json
{
  "email": "test@example.com",
  "password": "yourpassword",
  "userId": "user_001"
}
```
In production, the userId would be the unique MongoDB _id, but this sample app uses static IDs for demo purposes.

📦 Export as CSV
Go to the dashboard

Click on the Export CSV button in the header

Your transaction data will be downloaded in .csv format

🧠 Pagination Logic
Pagination is handled client-side using already fetched transaction data.

Ideal for small to medium datasets.

If the dataset grows, consider moving pagination to the server.

🛠 Tech Stack
Layer	Technology
Frontend	React, Vite, Aceternity UI
Backend	Node.js, Express.js
Database	MongoDB + Mongoose
Graphs	Recharts
Auth	JWT + bcrypt
API	RESTful APIs

🛡️ Security
Passwords are hashed using bcrypt

Auth is secured using JWT tokens

Environment variables are used for secrets

📬 Contact
Made with ❤️ by Juilee Shivaji Talekar


   





