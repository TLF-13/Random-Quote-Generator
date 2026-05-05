#созданиe GUI-приложения «Random Password Generator» на Python

 
import random
import string
 
def generate_password(length, use_digits, use_letters, use_special):
    chars = ''
    if use_digits: chars += string.digits
    if use_letters: chars += string.ascii_letters
    if use_special: chars += string.punctuation
    return ''.join(random.choices(chars, k=length))
 
# Сохранение истории в JSON
 import json
 
HISTORY_FILE = 'history.json'
 
def load_history():
    try:
        with open(HISTORY_FILE, 'r', encoding='utf-8') as f:
            return json.load(f)
    except FileNotFoundError:
        return []
 
def save_history(data):
    with open(HISTORY_FILE, 'w', encoding='utf-8') as f:
        json.dump(data, f, ensure_ascii=False, indent=2)
 

 
# Использование Git
 
Инициализируйте репозиторий:git init
git add .
git commit -m "Initial commit"
 
Создайте репозиторий на GitHub/GitLab и залейте проект:git remote add origin <ваш_репозиторий>
git push -u origin master
 
#Создание README.md
 
# Random Password Generator
 
**Автор:** Лилиана Рaхматуллина
 
