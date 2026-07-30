import telebot
from telebot.types import InlineKeyboardMarkup, InlineKeyboardButton, WebAppInfo

TOKEN = '8960409557:AAHJ_3CFWVgtWmu-Dttl7fEulvD6Ep4xUj4'

bot = telebot.TeleBot(TOKEN)

@bot.message_handler(commands=['start'])
def start(message):
    markup = InlineKeyboardMarkup()
    btn = InlineKeyboardButton(
        text="⚔️ Открыть Clans",
        web_app=WebAppInfo(url="https://babojbogdan3-droid.github.io/BSC-clans-/")
    )
    markup.add(btn)
    bot.send_message(
        message.chat.id,
        f"👋 Привет, {message.from_user.first_name}!\n"
        "Добро пожаловать в Block Strike Clans!\n"
        "Нажми на кнопку ниже, чтобы начать.",
        reply_markup=markup
    )

@bot.message_handler(func=lambda message: True)
def reply_all(message):
    bot.reply_to(message, "❓ Используй /start, чтобы открыть кланы.")

print("✅ Бот запущен!")
bot.polling(none_stop=True)