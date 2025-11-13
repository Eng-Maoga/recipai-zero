# 🍲 Zero Hunger Chef — AI Recipe Generator

A beautiful web application that generates nutritious, low-waste recipes from ingredients users already have. Built to support **UN SDG 2: Zero Hunger** by promoting sustainable food usage and reducing food waste.

**Live demo:** [https://hungerchef.up.railway.app/](https://hungerchef.up.railway.app/)
**Pitchdeck / Source:** [https://github.com/Eng-Maoga/recipai-zero.git](https://github.com/Eng-Maoga/recipai-zero.git)

## ✨ What it does

* **AI-Powered Recipe Generation** — Enter what ingredients you have and get creative, nutritious recipes.
* **Food Waste Reduction** — Turn leftovers into delicious meals and reduce household waste.
* **History & Search** — Save every generated recipe in a beautiful timeline and search/filter past recipes.
* **One-Click Regeneration** — Generate alternative variations of any saved recipe.

## 🎯 Key Features

### Core

* Ingredient-based recipe generation (AI)
* Unlimited usage — no paywall
* Responsive, accessible UI

### Recipe Experience

* Creative recipe names & descriptions
* Clear, step-by-step instructions
* Categorization (Protein, Carbs, Dessert, Vegetable)
* Copy-to-clipboard and share-friendly output

### UX & Design

* Modern, clean interface with subtle animations
* Floating ingredient animations and interactive cards
* Mobile-first, fully responsive design

## 🏗️ Tech Stack

**Backend**

* Python 3.8+
* Flask 2.3.3
* Flask-SQLAlchemy 3.0.5 / SQLAlchemy
* Flask-Login 0.6.3
* SQLite (development) — production-ready for PostgreSQL/MySQL

**Frontend**

* HTML5 / CSS3 (Grid & Flexbox)
* JavaScript (ES6+)
* Font Awesome, Google Fonts (Inter)

**AI & APIs**

* Google Gemini (primary model: `gemini-2.0-flash-001`)
* Multiple model fallback for reliability

## 📂 Project Structure

```
zero-hunger-chef/
├── app.py
├── requirements.txt
├── .env
├── static/
│   ├── css/style.css
│   ├── js/dashboard.js
│   ├── js/history.js
│   └── images/
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   └── history.html
├── instance/recipes.db
└── README.md
```
## 🚀 Quick Start

### Prerequisites

* Python 3.8+
* Google Gemini API key

### Install & Run (Development)

```bash
# Clone
git clone <repository-url>
cd zero-hunger-chef

# Create virtual environment
python -m venv venv
# macOS/Linux
source venv/bin/activate
# Windows
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Create .env file with variables (example below)
```

### Example `.env`

```
SECRET_KEY=your-secret-key-here
GOOGLE_API_KEY=your-gemini-api-key-here
```

### Initialize database

```bash
flask --app app.py _init_db
```

### Run

```bash
python app.py
# or
flask --app app.py run --debug
```

Open `http://127.0.0.1:5000` in your browser.

## 🎯 How to Use

1. Create an account (free, no payment required)
2. Go to **Dashboard** → enter ingredients (comma-separated)
3. Click **Generate Recipe** to receive AI-powered suggestions
4. View your Recipe History to search, copy, or regenerate variations

**Example input:** `chicken, rice, broccoli, garlic`
**Example output:** Full recipe with ingredients, steps, and cook time.

## 🔧 Configuration & Environment Variables

* `SECRET_KEY` — Flask secret key
* `GOOGLE_API_KEY` — Google Gemini API key
* `DATABASE_URL` — (optional) production DB connection string

## 🔒 Security

* Secure authentication with Flask-Login and password hashing
* Input validation and SQLAlchemy ORM to reduce risk of SQL injection
* Secure session management

## 🛠️ Development & Testing

* Use the debug server for local development.
* Useful dev endpoints (for debugging only):

  * `/api/history` — test history API (while logged in)
  * `/_debug_db`, `/_debug_models` — inspect DB & models locally

## 🚀 Deployment

**Production tips**

* Set `DEBUG=False`
* Use a WSGI server such as Gunicorn
* Use PostgreSQL or MySQL in production
* Configure reverse proxy (Nginx) and SSL

## 🤝 Contributing

Contributions welcome! Please:

1. Fork the repo
2. Create a feature branch
3. Add tests and documentation
4. Submit a pull request

## 🌟 Alignment with UN SDG 2

This project supports **Zero Hunger** by:

* Reducing food waste through creative recipe generation
* Encouraging nutritious, balanced meals
* Making cooking more accessible

## 🔮 Future Enhancements

* Recipe ratings & favorites
* Meal planning calendar
* Shopping list & pantry integration
* Nutritional analysis per recipe
* Multi-language support

## 📞 Support

If you need help:

* Check browser console & application logs
* Verify API keys and dependencies
* Open an issue on the GitHub repo: [https://github.com/Eng-Maoga/recipai-zero.git](https://github.com/Eng-Maoga/recipai-zero.git)

*Built with ❤️ to fight food waste and bring delicious, nutritious meals to more tables.*
