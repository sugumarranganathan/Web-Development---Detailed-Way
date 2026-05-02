CKD Prediction Web App (Django)
📁 Project Structure Explanation
🔹 1. Main Project Folder → ckdProject

This is the core Django project (backend configuration)

Contains:

settings.py → Project configuration (database, apps, etc.)
urls.py → Main routing (connects pages)
asgi.py / wsgi.py → Deployment files
__init__.py → Python package file



This folder manages the overall configuration and routing of the web application.

🔹 2. Application Folder → ckdApp

This is the actual functional web app (logic layer)

Contains:

models.py → Database structure (CKD data)
views.py → Backend logic (prediction processing)
forms.py → User input forms
urls.py → App-level routing
admin.py → Admin panel setup
apps.py → App config
tests.py → Testing


This app handles user input, processing, and prediction logic.

🔹 3. Database → db.sqlite3
Stores user data / prediction inputs


SQLite database is used for storing application data.

🔹 4. Machine Learning Model → finalized_model_ckd.sav
Pre-trained ML model
Used for predicting CKD


A trained machine learning model is integrated into the Django backend for prediction.

🔹 5. Dataset → prep.csv
Used to train the ML model
🔹 6. Entry File → manage.py
Used to run server and commands

Example:

python manage.py runserver
🔹 7. Requirements → requirements.txt
List of libraries (Django, sklearn, pandas, etc.)
 
Web App Works (FLOW)
Step-by-step:
User opens website
Fills CKD prediction form
Form data → sent to backend (views.py)
ML model (.sav) processes input
Prediction result returned
Displayed on webpage

Technologies Used
Frontend → HTML, CSS (Forms)
Backend → Django (Python)
Machine Learning → Scikit-learn
Database → SQLite
