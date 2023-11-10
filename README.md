from telegram import Update, ParseMode
from telegram import ReplyKeyboardMarkup, ReplyKeyboardRemove  # Обычная текстовая клавиатура
from telegram import InlineKeyboardButton, InlineKeyboardMarkup  # Инлайн-клавиатура
from telegram.ext import Updater, Dispatcher
from telegram.ext import MessageHandler, CommandHandler, CallbackQueryHandler
from telegram.ext import CallbackContext
from telegram.ext import Filters
import logging

def ask_name(update: Update , context:CallbackContext):
    pass

def get_name(update: Update , context:CallbackContext):
    pass

def ask_surename(update: Update , context:CallbackContext):
    user_id = update.message.from_user.id
    username = update.message.from_user.username
    logger.info(f"{username} {user_id} вызвал функцию ask_surname")
    answer = {
        f"Назови свою фамилию"
    }
    answer "\n".join(answer)
    update.message.reply_text(answer)

    return WAIT_SURNAME

def get_surename(update: Update , context:CallbackContext):
    pass

def ask_birthday(update: Update , context:CallbackContext):
    pass

def get_birthday(update: Update , context:CallbackContext):
    pass

def register(update: Update , context:CallbackContext):
    user_id = update.message.from_user.id
    username = update.message.from_user.username
    logger.info(f"{username} {user_id} вызвал функцию register")
    answer = {
        f"Зарегистрировал тебя!"
    }
    answer
    "\n".join(answer)
    update.message.reply_text(answer)
register_handler= ConversationHandler(
    entry_points=[CommandHandler(command:"register", ask_name)]
    #states{
    #WAIT_NAME :

#}

)
