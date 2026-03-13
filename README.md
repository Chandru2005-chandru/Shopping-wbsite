# Shopping-wbsite (PyShop)

A simple shopping/products website built with **Django**. It includes a `products` app with a `Product` model and a basic products listing page.

## Tech Stack
- Python
- Django (project: `pyshop`)
- SQLite (default local database: `db.sqlite3`)

## Features
- Product model with:
  - name
  - price
  - stock
  - image URL
- Basic products page (renders `index.html`) showing all products from the database
- Admin panel (`/admin/`)

## Routes
- `GET /admin/` — Django admin
- `GET /products/` — Products app (includes `products.urls`)

> Note: The repo currently includes the Django config files (`settings.py`, `urls.py`, `wsgi.py`, `asgi.py`) and product logic (`models.py`, `views.py`).
> If `products/urls.py` and templates (like `index.html`) are not in the repository yet, you’ll need to add them for `/products/` to work.

## Getting Started (Local Setup)

### 1) Clone the repository
```bash
git clone https://github.com/Chandru2005-chandru/Shopping-wbsite.git
cd Shopping-wbsite
```

### 2) Create and activate a virtual environment (recommended)
**Windows (PowerShell)**
```bash
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS/Linux**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3) Install dependencies
This repository does **not** currently include a `requirements.txt`. If you don’t have Django installed yet:

```bash
pip install django
```

(Optional) Create one for later:
```bash
pip freeze > requirements.txt
```

### 4) Run migrations
```bash
python manage.py migrate
```

### 5) Create an admin user (optional)
```bash
python manage.py createsuperuser
```

### 6) Start the development server
```bash
python manage.py runserver
```

Open:
- http://127.0.0.1:8000/admin/
- http://127.0.0.1:8000/products/

## Database
Uses SQLite by default:
- `db.sqlite3`

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you’d like to change.

## License
Add a license if you plan to share/redistribute this project (MIT is a common choice).