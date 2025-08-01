# CodelabS Checker API

> **Backend Project** · **Node.js + Express.js** · **Practical Development Challenge (USP CodeLab Boost)**

Welcome, Codelaber! 🎓

Before diving into the amazing journey of joining the best tech extension group at USP — the **USP CodeLab** — you must first help solve a pressing internal crisis.

## ❗ The Problem

Although we proudly carry the name **"Codelab"**, it seems that *no one knows how to spell it right*.

From emails to official documents and even within our community, the group name has been repeatedly miswritten as:

- Code labe  
- Cod lab  
- Codalab  
- Codeslab  
- Codeleb  
- And the most socially viral: **CodelabS**

Our project leads, **Shogo** and **Otavio**, shared their frustration during a Boost meeting — and that's when this challenge was born.

## 🚀 The Mission

Your mission is to build a **RESTful API** in **Node.js** to track and analyze all name submissions — both correct and incorrect — helping us quantify the scale of this spelling epidemic and take action.

This backend service will serve as the foundation for future integrations, such as websites or Telegram bots.

---

## 🧠 What You'll Build

A centralized, lightweight, and fun API that:

- Accepts name submissions  
- Logs whether they are correct or incorrect  
- Stores everything in a structured `.json` database  
- Can be used as a data source for dashboards, bots, or internal tools  

---

## 📂 Project Structure

```bash
.
├── nomes.json          # Local JSON "database"
├── index.js            # Main server file with all logic
├── package.json        # Dependencies and scripts
└── README.md           # You're here!
```

---

## ⚙️ Technologies Used

- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [fs](https://nodejs.org/api/fs.html) for file system handling
- [path](https://nodejs.org/api/path.html) for file paths

---

## 🛠️ How to Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/codelabs-checker-api.git
   cd codelabs-checker-api
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run the server:

   ```bash
   node index.js
   ```

4. Access the API at:  
   **`http://localhost:3000`**

---

## 📌 Endpoints

### `GET /`
Returns a simple welcome message to confirm the API is running.

---

### `POST /nomes`

Submits a name and stores whether it's correct or not.

**Request body:**

```json
{
  "nome": "Codelab"
}
```

**Responses:**

- `201 Created` → `{ "mensagem": "Nome correto!" }`
- `201 Created` → `{ "mensagem": "Nome incorreto!" }`

All submissions are timestamped and saved in `nomes.json`.

---

## 🧪 Example Data Output

```json
{
  "corretos": [
    {
      "nome": "Codelab",
      "data": "2025-08-01T11:21:57.752Z"
    }
  ],
  "incorretos": [
    {
      "nome": "CodelabS",
      "data": "2025-08-01T11:21:11.562Z"
    },
    {
      "nome": "Codelaber",
      "data": "2025-08-01T11:21:50.787Z"
    }
  ]
}
```

---

## 🤓 About the Challenge

This API was developed as part of the **Boost challenge**, a practical backend project proposed by **USP CodeLab**, the university’s most innovative and engaging technology group.

By combining problem-solving with technical implementation, this project aims to teach:

- RESTful API development  
- File-based data persistence  
- Express.js routing and logic handling  
- Fun ways to reinforce brand consistency 😉

---

## 👨‍💻 Author

Made with 💜 by a proud **Codelaber**, Bruno Zuffo.
