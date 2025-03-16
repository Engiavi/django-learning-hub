<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/75/Django_logo.svg" width="300" alt="Django Logo">
</p>

# 🚀 Django Learning Repository

## 📌 Introduction to Django  
Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. It is built with the **Don't Repeat Yourself (DRY)** principle and follows the **Model-View-Template (MVT)** architecture.  
Django provides an admin panel, authentication system, and many built-in features that simplify web development.

---

## 🔧 Setting Up Django  

![Install Django](https://img.shields.io/badge/Install%20Django-green?style=for-the-badge&logo=python)  
```bash
python -m pip install django
```
  
![Verify Django](https://img.shields.io/badge/Verify%20Django-blue?style=for-the-badge&logo=python)  
```python
import django
print(django.get_version())
```

---

## 🛠 Setting Up a Virtual Environment  

![Create Virtual Environment](https://img.shields.io/badge/Create%20Venv-orange?style=for-the-badge&logo=python)  
```bash
python -m venv venv
```

### ✅ Activate the Virtual Environment  

#### 🖥️ On Windows (Command Prompt)  
```cmd
venv\Scripts\activate
```

#### 🖥️ On Windows (PowerShell)  
```powershell
venv\Scripts\Activate.ps1
```

#### 🍏 On macOS/Linux  
```bash
source venv/bin/activate
```

### ❌ Deactivate the Virtual Environment  
```bash
deactivate
```


## ⚡ Running a Django Project  

  
![Install Django in Venv](https://img.shields.io/badge/Install%20Django%20inside%20Venv-purple?style=for-the-badge&logo=python)  
```bash
pip install django
```

### ✅ Create a new Django project  
```bash
django-admin startproject myproject
```

### ✅ Navigate into the project directory  
```bash
cd myproject
```

### ✅ Run the development server  
```bash
python manage.py runserver
```

Your Django project will be available at: **[http://127.0.0.1:8000/](http://127.0.0.1:8000/)**  