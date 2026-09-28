# SICLUS - Backend REST API

**SICLUS** (**S**chool **I**ntegrated **C**heck-in & **L**ogbook **U**nit **S**ystem) Backend is a high-performance RESTful API service developed for the **Department of Transportation of Mojokerto City (*Dinas Perhubungan Kota Mojokerto*)**.

It provides backend services for driver authentication, daily check-in validation, vehicle checklist management, checkpoint tracking, and administrative data reporting.

---

## Tech Stack

- **Framework**: [FastAPI](https://fastapi.tiangolo.com/) (Python)
- **Database & Storage**: [Supabase](https://supabase.com/) (PostgreSQL & Object Storage)
- **Authentication**: JWT (JSON Web Tokens) with `pyjwt` & `passlib` (bcrypt)
- **Data Export & Processing**: `pandas` & `openpyxl`
- **Server**: [Uvicorn](https://www.uvicorn.org/) ASGI

---

## Getting Started

### 1. Prerequisites
- Python 3.10+ (Python 3.12+ recommended)
- Virtual environment tool (`venv` or `uv`)

### 2. Environment Setup

Create and activate a virtual environment:

```bash
# Windows (PowerShell)
python -m venv .venv
.\.venv\Scripts\Activate.ps1

# Linux / macOS
python -m venv .venv
source .venv/bin/activate
```

Install required dependencies:

```bash
pip install -r requirements.txt
```

### 3. Environment Variables

Create a `.env` file in the root directory (based on `.env.example`):

```env
# Supabase Configuration
SUPABASE_URL=https://your-project-id.supabase.co
SUPABASE_KEY=your-supabase-key

# JWT Security
SECRET_KEY=your-jwt-secret-key-here
```

### 4. Running the Development Server

```bash
uvicorn app.main:app --reload
```

- API Base URL: `http://localhost:8000`
- Interactive API Documentation (Swagger UI): `http://localhost:8000/docs`
- Alternative API Documentation (ReDoc): `http://localhost:8000/redoc`

---

## Main API Endpoints

| Endpoint Prefix | Description |
| :--- | :--- |
| `/api/auth` | User login and JWT access token issuance |
| `/api/admin` | Operational dashboard, driver management, and route assignments |
| `/api/driver` | Driver profile, daily assignments, and checkpoint logging |
| `/api/laporan` | Vehicle checklist submissions and Excel report exports |

---

## Organization

Developed for the **Department of Transportation of Mojokerto City (*Dinas Perhubungan Kota Mojokerto*)**.
