# ProResume - Django Resume Builder 🚀

A professional, modern web application for building beautiful, ATS-friendly resumes in minutes. Built with Django, ProResume streamlines the resume creation process by providing an intuitive interface and professionally designed templates.

## ✨ Features

- **Intuitive Form Interface**: Easy-to-use form to capture all essential resume information
- **Professional Templates**: Multiple professionally designed resume templates
- **Real-time Preview**: See your resume as you build it
- **ATS-Friendly Output**: Resumes optimized for Applicant Tracking Systems
- **Export Options**: Download your resume as PDF
- **Multiple Sections Support**:
  - Personal Information
  - Professional Summary
  - Work Experience (Multiple entries)
  - Education (Multiple entries)
  - Skills
  - Projects
  - Certifications
  - Languages

## 🛠️ Tech Stack

- **Backend**: Django 3.x
- **Frontend**: HTML5, CSS3, Bootstrap 4
- **Database**: SQLite3 (Development) / PostgreSQL (Production)
- **Forms**: Django Crispy Forms
- **Additional Tools**: WhiteNoise, django-heroku (for deployment)

## 📋 Project Structure

```
proresume/
├── config/                 # Django configuration
│   ├── settings.py        # Main settings file
│   ├── urls.py            # URL routing
│   ├── wsgi.py            # WSGI configuration
│   └── __init__.py
├── apps/                  # Django applications
│   ├── resume/            # Main resume builder app
│   │   ├── models.py      # Database models
│   │   ├── views.py       # View functions
│   │   ├── forms.py       # Django forms
│   │   ├── urls.py        # App URL routing
│   │   ├── templates/     # HTML templates
│   │   ├── migrations/    # Database migrations
│   │   └── __init__.py
│   └── __init__.py
├── core/                  # Core utilities and helpers
├── static/                # Static files (CSS, JS, images)
│   └── css/
│       └── style.css
├── media/                 # User uploaded media
├── templates/             # Global templates
├── tests/                 # Test suite
├── docs/                  # Documentation
├── manage.py              # Django management script
├── requirements.txt       # Python dependencies
└── README.md             # This file
```

## 🚀 Quick Start

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)
- Virtual environment (recommended)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/priyanshusaini105/proresume.git
cd proresume
```

2. **Create and activate virtual environment**
```bash
# On Linux/Mac
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Apply migrations**
```bash
python manage.py migrate
```

5. **Create superuser (optional, for admin panel)**
```bash
python manage.py createsuperuser
```

6. **Run development server**
```bash
python manage.py runserver
```

7. **Access the application**
```
http://localhost:8000
```

## 📖 Usage

### Creating a Resume

1. Navigate to the home page
2. Click on "Create Resume" or "Build Your Resume"
3. Fill in your personal information
4. Add your work experience, education, and skills
5. Preview your resume
6. Download as PDF

### Admin Panel

Access the Django admin panel at `/admin` to:
- Manage resume templates
- View submitted resumes
- Manage user accounts

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the project root:

```
DEBUG=True
SECRET_KEY=your-secret-key-here
DATABASE_URL=sqlite:///db.sqlite3
ALLOWED_HOSTS=localhost,127.0.0.1
```

### Settings

Edit `config/settings.py` to configure:
- Database settings
- Email configuration
- Static files location
- Allowed hosts
- Time zone

## 📦 Dependencies

Key Python packages:
- `Django==3.x` - Web framework
- `django-crispy-forms` - Form rendering
- `django-heroku` - Heroku deployment support
- `whitenoise` - Static file serving
- `dj-database-url` - Database URL parsing

See `requirements.txt` for complete list.

## 🧪 Testing

Run tests with:

```bash
python manage.py test
```

Or with coverage:

```bash
coverage run --source='.' manage.py test
coverage report
```

## 🚢 Deployment

### Heroku Deployment

1. **Create Heroku app**
```bash
heroku create your-app-name
```

2. **Add Procfile** (already included)

3. **Deploy**
```bash
git push heroku main
```

### Other Platforms

For deployment to other platforms, refer to Django's deployment documentation.

## 📝 API Endpoints

- `GET /` - Home page
- `GET /resume/` - Resume form page
- `POST /resume/` - Submit resume data
- `/admin/` - Django admin panel



**Made with ❤️ by Priyanshu**
