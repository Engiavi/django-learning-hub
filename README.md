<p align="center">
  <a href="https://docs.djangoproject.com/en/stable/" target="_blank">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQZ7gi-Vovymw3486xkL9Oz9jBzCXEVyvPxIA&s#gh-light-mode-only" width="300" alt="Django Logo">
    <!-- <img src="https://codereview.doctor/django-logo.png#gh-dark-mode-only" width="300" alt="Django Logo"> -->
  </a>
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


---

### ✅ **README.md – Django Runserver Port Permission Issue & Fixes**

![Problem : Django Runserver Port Permission Issue](https://img.shields.io/badge/Problem:%20Django%20Runserver%20Port%20Permission%20Issue-white?style=for-the-badge&logo=python)  
```
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
Error: You don't have permission to access that port.

```
This happens because:
- The default port **8000** is **restricted** or **in use**.
- Your user **lacks administrative privileges**.
- A **firewall or security software** is blocking access.

---

## 🛠️ **Solutions to Fix This Issue**

### 1️⃣ **Run Django on a Different Port (Recommended)**
The simplest fix is to **change the port** Django runs on:
```bash
python manage.py runserver 8080
```
or
```bash
python manage.py runserver 127.0.0.1:9000
```

---

### 2️⃣ **Check If the Port Is Already in Use**
Django might be failing because **another process is using port 8000**.

#### 🔹 **On Windows**
Run:
```cmd
netstat -ano | findstr :8000
```
If a process is using it, **kill the process**:
```cmd
taskkill /PID <PID> /F
```

#### 🔹 **On macOS/Linux**
Run:
```bash
lsof -i :8000
```
If a process is using it, kill it:
```bash
kill -9 <PID>
```

---

### 3️⃣ **Run Django with Administrator Privileges**
If the port is restricted, try running Django as an **administrator**.

#### 🔹 **On Windows**
1. Open **Command Prompt as Administrator** (`Win + S` → search for **cmd** → Right-click → "Run as Administrator")
2. Run:
   ```cmd
   python manage.py runserver
   ```

#### 🔹 **On macOS/Linux**
Use `sudo`:
```bash
sudo python manage.py runserver
```
(You may need to enter your password)

---

### 4️⃣ **Check Firewall or Security Software**
Some **firewalls or security software** might be blocking Django.

#### 🔹 **On Windows**
1. Open **Control Panel** → **Windows Defender Firewall**  
2. Click **"Allow an app through Windows Firewall"**  
3. Ensure **Python** is **allowed** for both **private** and **public** networks  

#### 🔹 **On macOS/Linux**
Try temporarily disabling the firewall:
```bash
sudo ufw disable  # For Ubuntu/Debian
```
(Enable it again with `sudo ufw enable` after testing)

---

## 🎯 **Final Solution**
Try these solutions **one by one**. The **best & safest approach** is:
```bash
python manage.py runserver 8080
```
or  
```bash
python manage.py runserver 127.0.0.1:9000
```

 