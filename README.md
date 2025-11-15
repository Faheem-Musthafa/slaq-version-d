# To run the program:
<br />

<font color="red">

# 0⚡Initial Set Up 
</font>

<font color="green">

## 📦 Models
</font>

This reduce the processing delay
## (Terminal 1: `Download AI Models ~3GB`)
better use Command Prombt
### 1. Download AI model (first time only)
you can check if it downloaded on `C:\Users\[YOUR-USER-NAME]\.cache\huggingface\hub`
<br />
Activate enviornment (optional)
```shell
pip install transformers torch
```
Then run download_model.py
```shell
python download_model.py
```
<br />

<font color="red">

# 1⚡System Set Up 
</font>

<font color="green">

## 1) 🚚📨 Redis
</font>

## (Terminal 1: `Redis Server` )
Ensure Redis is installed
```shell
# Install Chocolatey first (if not installed)
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

# Install Redis using Chocolatey
choco install redis-64
```
### 1. Start Redis server

```shell
redis-server
```

<br />

<font color="green">

## 2) 🔁 Celery
</font>

AI Engine
## (Terminal 2: Activate the Python environment and run Celery)
### 1. Activate virtual environment

```shell
python -m venv venv
venv\Scripts\activate 
```
### 2. Install dependencies

```shell
pip install -r requirements.txt
```

### 3. Run celery

```shell
celery -A slaq_project worker --pool=solo -l info 
```

<br />

<font color="green">

## 3) 🦙 Run server
</font>

### 1. Activate virtual environment

```shell
python -m venv venv
venv\Scripts\activate 
```
### 2. Install dependencies

```shell
pip install -r requirements.txt
```

### 3. Uninstall some dependencies for some dependencies (gonna write this clear)

```sql
pip uninstall torch torchvision torchaudio torchcodec ffmpeg-python -y
pip install torch==2.5.1 torchvision==0.20.1 --index-url https://download.pytorch.org/whl/cu121 
pip install torchcodec
```
### 4. Run Server

```sql 
python manage.py runserver
```

---
Signing off.

