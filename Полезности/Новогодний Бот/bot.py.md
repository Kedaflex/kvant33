```python
import telebot
import schedule
import time
import datetime
import random
import threading

TOKEN = "ВСТАВЬ_СЮДА_СВОЙ_ТОКЕН"

bot = telebot.TeleBot(TOKEN)

users = {}
quotes = [
    "Пусть Новый год принесёт много радости! 🎁",
    "Верь в чудеса, и они случатся! ✨",
    "Новый год — время волшебства! 🪄",
    "Загадай желание, оно обязательно сбудется! ⭐",
    "Пусть снежинки принесут счастье! ❄️",
    "Дед Мороз уже в пути! 🎅",
    "Ёлка, мандарины и хорошее настроение! 🎄",
    "Скоро-скоро Новый год! 🎉",
]

def days_until_new_year():
    today = datetime.date.today()
    new_year = datetime.date(today.year + 1, 1, 1)
    if today.month == 1 and today.day == 1:
        return 0
    days_left = (new_year - today).days
    return days_left

@bot.message_handler(commands=['start'])
def start(message):
    user_name = message.from_user.first_name
    user_id = message.chat.id
    users[user_id] = user_name
    bot.send_message(
        user_id,
        f"Привет, {user_name}! 🎄\n"
        f"Я буду каждый день говорить тебе, сколько дней до Нового года!\n\n"
        f"Сейчас до Нового года: {days_until_new_year()} дней! 🎅"
    )

def send_morning_message():
    days = days_until_new_year()
    quote = random.choice(quotes)
    for user_id, user_name in users.items():
        try:
            text = f"Доброе утро, {user_name}! ☀️\n\n"
            text += f"🎄 До Нового года осталось: {days} дней\n\n"
            text += f"💫 {quote}"
            bot.send_message(user_id, text)
        except:
            pass

def send_12_oclock():
    today = datetime.date.today()
    if today.month == 12 and today.day == 31:
        for user_id, user_name in users.items():
            try:
                bot.send_message(user_id, f"🎄 {user_name}, готовься! Совсем скоро будет праздник! 🎁")
            except:
                pass

def send_16_oclock():
    today = datetime.date.today()
    if today.month == 12 and today.day == 31:
        for user_id, user_name in users.items():
            try:
                bot.send_message(user_id, f"✨ {user_name}, волшебство совсем близко! ✨")
            except:
                pass

def send_midnight():
    for user_id, user_name in users.items():
        try:
            bot.send_message(user_id, f"🎆🎆🎆\n\nС праздником, {user_name}!\n\n🎄 С НОВЫМ ГОДОМ!!! 🎄\n\n🎆🎆🎆")
        except:
            pass

schedule.every().day.at("09:00").do(send_morning_message)
schedule.every().day.at("12:00").do(send_12_oclock)
schedule.every().day.at("16:00").do(send_16_oclock)
schedule.every().day.at("00:00").do(send_midnight)

def run_schedule():
    while True:
        schedule.run_pending()
        time.sleep(60)

print("🎄 Бот запущен! 🎄")

thread = threading.Thread(target=run_schedule)
thread.start()

bot.polling(none_stop=True)
```
```
