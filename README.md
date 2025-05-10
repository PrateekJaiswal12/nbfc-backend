Here's a **complete `README.md`** for your **Node.js backend (contact form API)** that includes setup instructions, environment variables, endpoint documentation, and usage notes.

You can place this file in your `backend/` directory.

---

## ✅ `README.md` (For Your Contact Form Backend)

```md
# NBFC Contact Backend API

This is the backend server for the **NBFC Contact Form**. It handles form submissions, stores contact messages in MongoDB, and provides APIs for admin review and management.

---

## 🚀 Tech Stack

- Node.js
- Express.js
- MongoDB (via Mongoose)
- Nodemon (for development)
- CORS

---

## 📁 Project Structure

```

backend/
├── models/
│   └── contactUs.model.js        # Mongoose schema for contact messages
├── routes/
│   └── contact.js                # API routes for handling messages
├── server.js                     # Express app entry point
├── .env                          # Environment config
└── README.md                     # You're here

````

---

## 🔧 Setup Instructions

### 1. Clone the repo
```bash
git clone <your-repo-url>
cd backend
````

### 2. Install dependencies

```bash
npm install
```

### 3. Create a `.env` file

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/nbfc-contact
```

> Replace the `MONGO_URI` with your own MongoDB connection string if needed.

### 4. Start the server

#### In development:

```bash
npx nodemon server.js
```

#### In production:

```bash
node server.js
```

---

## 🔌 API Endpoints

### `POST /api/contact`

Save a new contact form message.

#### Request Body

```json
{
  "name": "Prateek Jaiswal",
  "email": "prateek@example.com",
  "subject": "Inquiry",
  "message": "Hello, I would like to connect."
}
```

#### Response

```json
{
  "success": true,
  "message": "Message sent successfully",
  "data": { ... }
}
```

---

### `GET /api/contact/admin`

Get all contact messages (for admin panel).

#### Response

```json
{
  "success": true,
  "count": 4,
  "data": [ ... ]
}
```

---

### `GET /api/contact/:id`

Fetch a single contact message by ID.

---

### `PATCH /api/contact/:id/status`

Update the message status to `pending`, `read`, or `replied`.

#### Request Body

```json
{
  "status": "read"
}
```

---

### `DELETE /api/contact/:id`

Delete a contact message.

---

## 🌐 CORS

CORS is enabled to allow frontend access from Vite (localhost:5173 by default). You can restrict or configure it in `server.js`:

```js
app.use(cors({
  origin: 'http://localhost:5173',
  credentials: true
}));
```

---

## ✅ Testing

You can test API endpoints using tools like:

* [Postman](https://www.postman.com/)
* [Thunder Client](https://www.thunderclient.com/)
* Or directly from your frontend app using Axios or Fetch.

---

## 🧑‍💻 Author

Built by [Prateek Jaiswal](mailto:prateekjaiswalpj07@gmail.com)

---

## 📜 License

MIT — free to use and modify.

```

---

Let me know if you want a similar `README.md` for the frontend as well.
```
