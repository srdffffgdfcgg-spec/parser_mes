<h1 align="center">🤖 Telegram Job Parser</h1>
<p align="center">
  Автоматичний парсер для пошуку людей, які шукають роботу у Telegram-групах.<br>
  Зберігає результати у CSV та дублює у <b>"Збережені повідомлення"</b> Telegram.
</p>

---

## ✨ Можливості

✔️ Підключення до Telegram через ваш акаунт  
✔️ Парсинг будь-яких груп за посиланнями  
✔️ Пошук за ключовими словами (*«шукаю роботу», «ищу работу», «подработка» і т.д.*)  
✔️ Збереження у CSV (Excel / Google Sheets)  
✔️ Автоматичне відправлення результатів у "Збережені" Telegram  
✔️ Підтримка Windows, MacOS, Linux  

---

## 🔧 Що потрібно

| Необхідно              | Де взяти                                                                 |
|------------------------|-------------------------------------------------------------------------|
| **Python 3.10+**       | [python.org/downloads](https://www.python.org/downloads/)                |
| **API ID + HASH**      | [my.telegram.org](https://my.telegram.org) → *API development tools*    |
| **Бібліотека Telethon**| Встановлюється командою `pip install telethon`                          |

---

## 🚀 Встановлення та запуск

### 1. Скачайте Python
- **Windows:** під час встановлення обов’язково поставте галочку *Add to PATH*  
- **MacOS:**  
  ```bash
  brew install python3

  Linux (Ubuntu/Debian):

sudo apt update && sudo apt install python3 python3-pip -y

2. Клонування репозиторію
git clone https://github.com/username/telegram-job-parser.git
cd telegram-job-parser

3. Встановіть бібліотеки
pip install telethon


💡 Рекомендовано створити віртуальне середовище:

python -m venv venv
source venv/bin/activate     # macOS/Linux
venv\Scripts\activate        # Windows
pip install telethon

4. Налаштуйте parser.py

Відкрийте файл та замініть:

api_id = 11111111
api_hash = '000000000000000000000'


на свої дані з my.telegram.org
.

У секції group_links додайте групи для парсингу:

group_links = [
    'https://t.me/Nasva_Grupu',
    'https://t.me/інша_група'
]

5. Запуск скрипта

Windows

python parser.py


macOS / Linux

python3 parser.py

⚙️ Як працює

Скрипт підключається до вашого акаунта Telegram

Заходить у вказані групи

Переглядає повідомлення

Фільтрує ті, де є ключові слова («шукаю роботу», «ищу работу», «подработка»)

Зберігає знайдені дані:

у contacts_<назва_групи>.csv (по групах)

у contacts_all.csv (з усіх груп)

Надсилає результати у "Збережені повідомлення" Telegram

Якщо файл великий — відправляє його як документ

⏹ Зупинка роботи

Для завершення натисніть у терміналі:

Ctrl + C


Скрипт збереже всі знайдені контакти перед виходом.

📊 Приклад результату (CSV)
message_id	message	username	first_name	last_name	phone	group
123456	"Шукаю роботу в Києві"	ivan_job	Ivan	Petrenko	+380...	Nasva_Grupu
789012	"Ищу работу удаленно"	maria_dev	Maria	–	None	Nasva_Grupu
🖼 Скріншоти (опційно)

📂 CSV у Excel
💬 Повідомлення у "Збережених" Telegram

(Додай свої скріншоти сюди для наочності)

📜 Ліцензія

Вільне використання для особистих та навчальних цілей.


