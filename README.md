# final---project
import telebot
from telebot import types
import pandas as pd
import requests
from bs4 import BeautifulSoup
bot = telebot.TeleBot('5072802244:AAGeIS1blxAT_0w54i3XQCpwo1Ncc-GVhBw')

# Start Code Optima Bank
optima_bank = 'https://www.optimabank.kg/ru/'
headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page = requests.get(optima_bank, headers=headers)
soup = BeautifulSoup(full_page.content, 'html.parser')
convert = soup.findAll('span', {'class': 'up'})
rr = '''                            
    Курс   Продажа   Покупка
    USD  {0}   {1}
    EUR  {2}   {3}
    RUB  {4}    {5}
    KZT  {6}    {7}    

    '''.format(convert[0].text, convert[1].text, convert[2].text, convert[3].text, convert[4].text, convert[5].text,
               convert[6].text, convert[7].text)

rrdfefgf = '''                            
      Rate   Sale   Purchase
      USD    {0}    {1}
      EUR    {2}    {3}
      RUB    {4}    {5}
      KZT    {6}    {7}

    '''.format(convert[0].text, convert[1].text, convert[2].text, convert[3].text, convert[4].text, convert[5].text,
               convert[6].text, convert[7].text)

tolubai_bank = 'https://www.tolubaybank.kg'
headers1 = {
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page1 = requests.get(tolubai_bank, headers=headers1)
soup1 = BeautifulSoup(full_page1.content, 'html.parser')
convert1 = soup1.findAll('span', {'class': 'up'})
gg = '''                            
    Курс   Продажа   Покупка
    USD  {0}   {1}
    EUR  {2}   {3}
    RUB  {4}    {5}
    KZT  {6}    {7}    

    '''.format(convert1[0].text, convert1[1].text, convert1[2].text, convert1[3].text, convert1[4].text,
               convert1[5].text, convert1[6].text, convert1[7].text)

ggasdqwqdw = '''                        
          Rate   Sale   Purchase
      USD    {0}    {1}
      EUR    {2}    {3}
      RUB    {4}    {5}
      KZT    {6}    {7}
    '''.format(convert1[0].text, convert1[1].text, convert1[2].text, convert1[3].text, convert1[4].text,
               convert1[5].text, convert1[6].text, convert1[7].text)



bakai_bank = 'https://bakai.kg/ru/'
headers2 = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page2 = requests.get(bakai_bank, headers = headers2)
soup2 = BeautifulSoup(full_page2.content, 'html.parser')
convert2_buy = soup2.findAll('td', {'class': 'currency_buy'})
convert2_sell = soup2.findAll('td', {'class': 'currency_sell'})
rrrr = '''
    Курс   Продажа   Покупка
    USD    {0}    {1}
    EUR    {2}    {3}
    RUB    {4}    {5}
    KZT    {6}    {7}
'''.format(convert2_buy[0].text.split(), convert2_sell[0].text.split(), convert2_buy[1].text.split(), convert2_sell[1].text.split(), convert2_buy[2].text.split(),convert2_sell[2].text.split(), convert2_buy[3].text.split(), convert2_sell[3].text.split())

rrrfdfdr = '''
      Rate   Sale   Purchase
      USD    {0}    {1}
      EUR    {2}    {3}
      RUB    {4}    {5}
      KZT    {6}    {7}
'''.format(convert2_buy[0].text.split(), convert2_sell[0].text.split(), convert2_buy[1].text.split(), convert2_sell[1].text.split(), convert2_buy[2].text.split(),convert2_sell[2].text.split(), convert2_buy[3].text.split(), convert2_sell[3].text.split())


demir_bank = 'https://demirbank.kg/ru'
headers3 = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page3 = requests.get(demir_bank, headers = headers3)
soup3 = BeautifulSoup(full_page3.content, 'html.parser')
convert3 = soup3.findAll('td')

rfgc = '''
    Курс   Продажа   Покупка
    USD    {0}    {1}
    EUR    {2}    {3}
    RUB    {4}    {5}
    KZT    {6}    {7}
'''.format(convert3[3].text, convert3[4].text, convert3[5].text, convert3[6].text,convert3[7].text, convert3[8].text, convert3[11].text, convert3[12].text)

rfgcfefef = '''
      Rate   Sale   Purchase
      USD    {0}    {1}
      EUR    {2}    {3}
      RUB    {4}    {5}
      KZT    {6}    {7}
'''.format(convert3[3].text, convert3[4].text, convert3[5].text, convert3[6].text,convert3[7].text, convert3[8].text, convert3[11].text, convert3[12].text)


rsk_bank = 'https://www.rsk.kg/'
headers4 = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page4 = requests.get(rsk_bank, headers = headers4)
soup4 = BeautifulSoup(full_page4.content, 'html.parser')
convert4 = soup4.findAll('div', {'class': 'price'})
hhhhhhhh = '''
    Курс   Продажа   Покупка
    USD    {0}    {1}
    EUR    {2}    {3}
    RUB    {4}    {5}
    KZT    {6}    {7}
'''.format(convert4[0].text, convert4[1].text, convert[2].text, convert[3].text, convert4[4].text, convert4[5].text, convert4[6].text,convert4[7].text)
hhhhhhhh1111 = '''
      Rate   Sale   Purchase
      USD    {0}    {1}
      EUR    {2}    {3}
      RUB    {4}    {5}
      KZT    {6}    {7}
'''.format(convert4[0].text, convert4[1].text, convert[2].text, convert[3].text, convert4[4].text, convert4[5].text, convert4[6].text,convert4[7].text)

companion_bank = 'https://www.kompanion.kg/ru/'
headers5 = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page5 = requests.get(companion_bank, headers = headers5)
soup5 = BeautifulSoup(full_page5.content, 'html.parser')
convert5 = soup5.findAll('td')
adan = '''
    Курс   Продажа   Покупка
    USD    {0}    {1}
    EUR    {2}    {3}
    RUB    {4}    {5}
    KZT    {6}    {7}
'''.format(convert5[5].text, convert5[6].text, convert5[9].text, convert5[10].text, convert5[13].text, convert5[14].text, convert5[17].text,convert5[18].text)
adan111 = '''
      Rate   Sale   Purchase
      USD    {0}    {1}
      EUR    {2}    {3}
      RUB    {4}    {5}
      KZT    {6}    {7}
'''.format(convert5[5].text, convert5[6].text, convert5[9].text, convert5[10].text, convert5[13].text, convert5[14].text, convert5[17].text,convert5[18].text)


esb_bank = 'https://esb.kg/#'
headers6 = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36'}
full_page6 = requests.get(esb_bank,  headers = headers6)
soup6 = BeautifulSoup(full_page6.content, 'html.parser')
convert6 = soup6.findAll('div', {'class': 'esb'})
r = convert6[0].text.split()

esb_bank  = '''
    Курс   Продажа   Покупка
    USD    {0}    {1}
    EUR    {2}    {3}
    RUB    {4}    {5}
    KZT    {6}    {7}
'''.format(r[10], r[11],r[13], r[14], r[16], r[17],r[19], r[20])
esb_bank11  = '''
    Rate   Sale   Purchase
    USD    {0}    {1}
    EUR    {2}    {3}
    RUB    {4}    {5}
    KZT    {6}    {7}
'''.format(r[10], r[11],r[13], r[14], r[16], r[17],r[19], r[20])

# Finish Code


@bot.message_handler(commands=['start'])
def start(message):
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True, row_width=3)
    btn1 = types.KeyboardButton('Русский')
    btn2 = types.KeyboardButton('English')
    markup.add(btn1, btn2)
    send_mess = f"<b> Привет {message.from_user.first_name} {message.from_user.last_name}</b>! \n Выберите язык! / Choose language"
    bot.send_message(message.chat.id, send_mess, parse_mode='html', reply_markup=markup)

@bot.message_handler(content_types = ['text'])
def mess(message):
    get_message_bot = message.text.strip().lower()
    if get_message_bot == 'english':
        markup = types.ReplyKeyboardMarkup(resize_keyboard=True, row_width=3)
        btn1 = types.KeyboardButton('Optima Bank')
        btn2 = types.KeyboardButton('Tolubai Bank')
        btn3 = types.KeyboardButton('Bakai Bank')
        btn4 = types.KeyboardButton('Demir Bank')
        btn5 = types.KeyboardButton('RSK Bank')
        btn6 = types.KeyboardButton('Companion Bank')
        btn7 = types.KeyboardButton('ESB Bank')
        btn8  =types.KeyboardButton('Menu')
        markup.add(btn1, btn2, btn3, btn4, btn5, btn6, btn7, btn8)
        final_message = 'Choose Bank'
        bot.send_message(message.chat.id, final_message, parse_mode='html', reply_markup=markup)
    if get_message_bot == 'русский':
        markup = types.ReplyKeyboardMarkup(resize_keyboard=True, row_width=3)
        btn1 = types.KeyboardButton('Оптима Банк')
        btn2 = types.KeyboardButton('Толубай Банк')
        btn3 = types.KeyboardButton('Бакай Банк')
        btn4 = types.KeyboardButton('Демир Банк')
        btn5 = types.KeyboardButton('РСК Банк')
        btn6 = types.KeyboardButton('Компанион Банк')
        btn7 = types.KeyboardButton('ЕСБ Банк')
        btn8 = types.KeyboardButton('Меню')
        markup.add(btn1, btn2, btn3, btn4, btn5, btn6, btn7, btn8)
        final_message = 'Выберите банк'
        bot.send_message(message.chat.id, final_message, parse_mode='html', reply_markup=markup)
        bot.send_message(message.chat.id,final_message, parse_mode='html', reply_markup=markup)
    if get_message_bot == 'бакай банк':
        bot.send_message(message.chat.id, rrrr, parse_mode= 'html' )
    if get_message_bot == 'толубай банк':
        bot.send_message(message.chat.id, gg, parse_mode= 'html')
    if get_message_bot == 'демир банк':
        bot.send_message(message.chat.id, rfgc, parse_mode= 'html')
    if get_message_bot == 'оптима банк':
        bot.send_message(message.chat.id, rr, parse_mode= 'html')
    if get_message_bot == 'рск банк':
        bot.send_message(message.chat.id, hhhhhhhh, parse_mode= 'html')
    if get_message_bot == 'компанион банк':
        bot.send_message(message.chat.id, adan, parse_mode='html')
    if get_message_bot == 'есб банк':
        bot.send_message(message.chat.id, esb_bank, parse_mode= 'html')

    if get_message_bot == 'bakai bank':
        bot.send_message(message.chat.id, rrrfdfdr, parse_mode= 'html')
    if get_message_bot == 'tolubai bank':
        bot.send_message(message.chat.id, ggasdqwqdw, parse_mode= 'html')
    if get_message_bot == 'demir bank':
        bot.send_message(message.chat.id, rfgcfefef, parse_mode= 'html')
    if get_message_bot == 'optima bank':
        bot.send_message(message.chat.id, rrdfefgf, parse_mode= 'html')
    if get_message_bot == 'rsk bank':
        bot.send_message(message.chat.id, hhhhhhhh1111, parse_mode= 'html')
    if get_message_bot == 'companion bank':
        bot.send_message(message.chat.id, adan111, parse_mode= 'html')
    if get_message_bot == 'esb bank':
        bot.send_message(message.chat.id, esb_bank11, parse_mode= 'html')

    if get_message_bot == 'меню' or get_message_bot == 'menu':
        markup = types.ReplyKeyboardMarkup(resize_keyboard=True, row_width=3)
        btn1 = types.KeyboardButton('Русский')
        btn2 = types.KeyboardButton('English')
        markup.add(btn1, btn2)
        send_mess = f"<b> Привет {message.from_user.first_name} {message.from_user.last_name}</b>! \n Выберите язык интерфейса!"
        bot.send_message(message.chat.id, send_mess, parse_mode='html', reply_markup=markup)
bot.polling(none_stop=True)
