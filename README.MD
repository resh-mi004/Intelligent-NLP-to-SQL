
# 🧠 Intelligent SQL Assistant: Natural Language to Database Query System

[![Streamlit App](https://img.shields.io/badge/Try%20It%20Live-Streamlit-ff4b4b?style=flat-square&logo=streamlit&logoColor=white)](https://intelligent-sql-assistant-natural-language-to-database-query-s.streamlit.app)

An AI-powered web application that allows users to convert natural language queries into SQL queries and retrieve results from a connected database. This tool bridges the gap between human language and database interaction, enabling non-technical users to access structured data efficiently.

---

## 🚀 Demo

👉 **Live App:** [Intelligent SQL Assistant](https://intelligent-sql-assistant-natural-language-to-database-query-s.streamlit.app)

---

## 🧩 Features

- ✅ Convert natural language to SQL queries using LLMs
- ✅ View both the **generated SQL** and **query results**
- ✅ Simple and clean Streamlit UI
- ✅ Supports dynamic database schema
- ✅ Includes sample `users` and `products` tables for testing
- ✅ Error handling for invalid queries

---

## 🏗️ How It Works

1. **User Input**: User enters a query in plain English (e.g., “Show all products with price greater than 500”).
2. **LLM Translation**: The app uses an LLM to convert the input to a valid SQL query.
3. **SQL Execution**: The SQL query is executed on the connected SQLite database.
4. **Display**: Results and the SQL query are shown to the user in a readable format.

---

## 📊 Sample Tables

### `users`
```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    age INTEGER,
    email TEXT
);

INSERT INTO users (name, age, email)
VALUES 
('Alice', 25, 'alice@example.com'),
('Bob', 30, 'bob@example.com');
```

### `products`
```sql
CREATE TABLE products (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    price REAL,
    stock INTEGER
);

INSERT INTO products (name, price, stock)
VALUES 
('Laptop', 799.99, 10),
('Headphones', 199.99, 50),
('Mouse', 25.50, 100);
```

---

## ❓ Example Questions You Can Ask

- "Show all users older than 25"
- "List all products with stock less than 20"
- "What is the average price of products?"
- "Count the number of users"
- "Get the names of products priced above 200"

---

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **Backend**: Python + SQLite
- **AI Engine**: Large Language Model (LLM) via OpenAI or compatible provider
- **Database**: SQLite (local and in-memory)

---

## 📁 Project Structure

```
├── main.py                   # Streamlit app entry point
├── database.db               # SQLite database file
├── models/                   # Folder for prompt and LLM logic
│   └── llm_utils.py
├── utils/                    # Utility functions for SQL execution and display
│   └── sql_executor.py
├── requirements.txt
└── README.md                 # This file
```

---

## ⚙️ Setup & Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/intelligent-sql-assistant.git
cd intelligent-sql-assistant
```

### 2. Create Virtual Environment
```bash
python -m venv venv
# Activate environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the App
```bash
streamlit run main.py
```

---

## 🔐 Environment Variables (Optional for OpenAI Integration)
If using OpenAI or another LLM API:

```env
OPENAI_API_KEY=your_openai_api_key
```

---

## 📌 Future Improvements

- 🔄 Add support for other databases (PostgreSQL, MySQL)
- 🧠 Model fine-tuning with user feedback
- 🧾 Natural language INSERT, UPDATE, DELETE support
- 📊 Visualize SQL results (charts and graphs)

---

## 🙋‍♂️ Author

**Thanka Bharathi T M**  
Data Scientist & AI Developer  
🌐 [LinkedIn](https://www.linkedin.com/in/thankabharathi) | ✨ [Portfolio](https://thankabharathi.vercel.app)

---

## 🪪 License

This project is licensed under the MIT License - see the LICENSE file for details.
