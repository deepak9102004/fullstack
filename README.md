# Fullstack Todo App

A minimal fullstack example:
- **Backend:** Python (Flask) — REST API + serves the frontend
- **Frontend:** HTML, CSS, JavaScript (vanilla, no framework)

## Project structure

```
fullstack-todo/
├── app.py              # Flask backend (routes + REST API)
├── requirements.txt    # Python dependencies
├── templates/
│   └── index.html      # Main page
└── static/
    ├── style.css        # Styling
    └── script.js        # Frontend logic (calls the API with fetch)
```

## Setup & run

1. (Optional but recommended) Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # on Windows: venv\Scripts\activate
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the app:
   ```bash
   python app.py
   ```

4. Open your browser at **http://127.0.0.1:5000**

## How it works

- The frontend (`index.html` + `script.js`) sends HTTP requests using `fetch()`
  to a REST API served by Flask.
- The backend stores todos in memory (a Python list) — great for learning,
  but data resets whenever the server restarts.
- API endpoints:
  | Method | Endpoint            | Description          |
  |--------|----------------------|-----------------------|
  | GET    | `/api/todos`         | List all todos       |
  | POST   | `/api/todos`         | Add a new todo       |
  | PATCH  | `/api/todos/<id>`    | Update (toggle/edit) |
  | DELETE | `/api/todos/<id>`    | Delete a todo        |

## Next steps to extend it

- Swap the in-memory list for a real database (SQLite via `sqlite3` or `SQLAlchemy`)
- Add user accounts/authentication
- Deploy the Flask app (e.g. Render, Railway, PythonAnywhere) and serve the frontend from it
