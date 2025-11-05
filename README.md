# 🐍 DjangoStarter

A minimal Django starter project featuring a simple Tweet application.
Perfect for learning Django fundamentals, demos, or as a foundation for small projects.

---

## 📂 Project Overview

This repository provides a lightweight Django setup that includes:
- A basic Tweet app (tweet/)
- Templates and media uploads
- Preconfigured settings for local development

### Project Structure
<img width="444" height="429" alt="image" src="https://github.com/user-attachments/assets/2701d45f-13ef-46de-89a7-93eb75ddcb0a" />

--- 

## ⚙️ Quick Summary

- Inputs: Python 3.8+ and a virtual environment
- Outputs: Running development server with a working Tweet app
- Error Modes: Missing dependencies, migrations, or media folder permissions
- Success Indicator: The site runs locally when you execute python manage.py runserver

---

## 🧩 Prerequisites

- Python 3.8+
- pip package manager
- (Optional) Git for version control

- If a requirements.txt file is missing, install Django manually and generate one using:
```bash
pip install django
pip freeze > requirements.txt
```

---

## 🚀 Setup Instructions (Windows PowerShell)

Run the following commands from the project root:

1. **Create and activate a virtual environment**
```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. **Install dependencies**
- if (Test-Path requirements.txt) { pip install -r requirements.txt } else { pip install django }

3. **Apply migrations**
```bash
python manage.py migrate
```

4. **Create a superuser**
```bash
python manage.py createsuperuser
```

5. **Start the development server**
```bash
python manage.py runserver
```

✅ Tip:
After installing new dependencies, update your requirements.txt:
```bash
pip freeze > requirements.txt
```

---

## 🧪 Common Tasks

- Run Tests:
```bash
python manage.py test
```

- Collect Static Files (for production):
```bash
python manage.py collectstatic
```

---

## 🖼️ Media & File Uploads

- Uploaded files are stored in the media/ directory.
- Ensure your environment has write permissions, and confirm these settings in djangoStarter/settings.py:
```bash
MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
```

---

## 🎨 Templates
- Global templates: templates/
- App templates: tweet/templates/
The base HTML layout is located at templates/layout.html, extended by other pages.

---

## 🌐 Deployment Notes

For production deployment:

1. Set:
```bash
DEBUG = False
ALLOWED_HOSTS = ['your-domain.com', 'www.your-domain.com']
```

2. Use a proper WSGI/ASGI server (e.g., Gunicorn or Uvicorn)
3. Serve static and media files using Nginx, Apache, or a CDN
4. Secure the app with environment variables and HTTPS

--- 

## 🧭 Recommended Next Steps

- Add a requirements.txt with pinned versions
- Create a CONTRIBUTING.md for collaboration guidelines
- Add a CI workflow (e.g., GitHub Actions) to run tests automatically
- Include a LICENSE file for open-source distribution
- Configure .env files for secret management

---

## 📜 License
This project is distributed under the MIT License.

---

## Made with ❤️ using Django

A simple, clean foundation for your next web project.
