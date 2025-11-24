# Task API

A simple Django REST Framework backend for managing tasks.

## Setup

1. **Clone the repository**
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Configure environment variables**  
   Edit `.env` for your secret key and settings.

4. **Run migrations**
   ```bash
   python manage.py migrate
   ```

5. **Start the server**
   ```bash
   python manage.py runserver
   ```

## Docker

Build and run with Docker Compose:

```bash
docker-compose up --build
```

For production (port 8069):

```bash
docker-compose -f docker-compose.prod.yaml up --build
```

## API Endpoints

| Method | Endpoint           | Description                          |
|--------|--------------------|--------------------------------------|
| GET    | `/tasks/`          | List all tasks                       |
| POST   | `/tasks/`          | Create a new task                    |
| GET    | `/tasks/{id}/`     | Retrieve a task by ID                |
| PUT    | `/tasks/{id}/`     | Update a task (title & description)  |
| PATCH  | `/tasks/{id}/`     | Toggle task completed status only    |
| DELETE | `/tasks/{id}/`     | Delete a task                        |

## Environment Variables

Example `.env`:
```
SECRET_KEY="your-secret-key"
DEBUG=True
DATABASE_NAME=db.sqlite3
```

## License

MIT