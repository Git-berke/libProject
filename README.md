## Features

*   **Book Management:** Add, remove, update, and view book details.
*   **User Authentication:** User registration and login.
*   **Borrowing System:** Manage book borrowing and returns.
*   **Messaging:** Internal messaging system.
*   **Reviews:** Allow users to review books.
*   **Favorites:** Allow users to mark books as favorites.

*(Based on the router names in `Backend/main.py`. Specific features might vary.)*

## Tech Stack

### Frontend

*   **React:** JavaScript library for building user interfaces.
*   **Vite:** Next-generation frontend tooling (dev server, bundler).
*   **TypeScript:** Superset of JavaScript that adds static typing.
*   **Axios:** Promise-based HTTP client for making API requests.
*   **React Router DOM:** For client-side routing.
*   **Zustand:** Small, fast, and scalable bearbones state-management solution.
*   **Tailwind CSS:** Utility-first CSS framework.
*   **ESLint:** Pluggable linting utility for JavaScript and JSX.

### Backend

*   **FastAPI:** Modern, fast (high-performance) web framework for building APIs with Python.
*   **SQLAlchemy:** SQL toolkit and Object Relational Mapper (ORM).
*   **Uvicorn:** ASGI server for running FastAPI applications.
*   **Python:** Programming language.

### Database
Sql Server
## Prerequisites

*   Node.js and npm (or yarn) for the frontend.
*   Python and pip for the backend.
*   A relational database compatible with SQLAlchemy (e.g., PostgreSQL, MySQL, SQLite, SQL Server).

## Getting Started

### Backend Setup

1.  **Navigate to the backend directory:**
    ```bash
    cd KütüphaneSistemiReact/Backend
    ```
2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3.  **Install dependencies:**
    (Assuming a `requirements.txt` file exists. If not, you'll need to create one based on imports in `.py` files: `fastapi`, `uvicorn[standard]`, `sqlalchemy`, potentially a database driver like `psycopg2-binary` or `mysqlclient`)
    ```bash
    pip install -r requirements.txt
    ```
    If no `requirements.txt`, install common packages:
    ```bash
    pip install fastapi uvicorn[standard] sqlalchemy python-dotenv
    # Add database specific driver e.g. pip install psycopg2-binary
    ```
4.  **Configure your database:**
    *   Update `database.py` and potentially `config.py` with your database connection details.
    *   Ensure your database server is running.
5.  **Run the backend server:**
    The `main.py` file is configured to run with Uvicorn on `http://127.0.0.1:8000`.
    ```bash
    python main.py
    ```
    Or directly with uvicorn:
    ```bash
    uvicorn main:app --reload --host 127.0.0.1 --port 8000
    ```

### Frontend Setup

1.  **Navigate to the frontend directory:**
    ```bash
    cd KütüphaneSistemiReact/Frontend
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    # or
    # yarn install
    ```
3.  **Run the development server:**
    ```bash
    npm run dev
    # or
    # yarn dev
    ```
    The frontend will typically be available at `http://localhost:5173`.

## API Endpoints

The backend exposes various API endpoints. Refer to the FastAPI auto-generated documentation (usually at `http://127.0.0.1:8000/docs` or `http://127.0.0.1:8000/redoc` when the backend is running) for a detailed list of endpoints and their usage.

Key routers include:
*   `/users`
*   `/borowed` (likely `/borrowed`)
*   `/books`
*   `/messages`
*   `/reviews`
*   `/favorites`

## Building for Production

### Frontend

```bash
npm run build
```
This will create a `dist` folder in `KütüphaneSistemiReact/Frontend` with the production-ready static assets.

### Backend

For production, you would typically run the FastAPI application using a production-grade ASGI server like Gunicorn with Uvicorn workers behind a reverse proxy (e.g., Nginx).

## Contributing

(You can add guidelines for contributing to the project here if it's open for collaboration.)
