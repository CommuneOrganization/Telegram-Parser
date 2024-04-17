<p align="center">
    <a href="https://obscure88.github.io/commune.github.io/"><img src="https://static.tildacdn.com/tild3562-3164-4038-a135-313766303065/la_telegram.png" width="100px"/></a>
    <h3 align="center">Telegram Parser</h3>
</p>

<p align="center">
  Парсинг пользователей
  <br/>
  из ваших чатов и каналов
</p>

<p align="center">
    <a href="https://t.me/+1uaXH7-nquFjNWJh">
        <img src="https://img.shields.io/badge/telegram-white?style=flat&logo=telegram&logoColor=%23000000&labelColor=%23ffffff&color=%23000000"/></a>
    <a href="https://youtube.com/@communez">
        <img src="https://img.shields.io/badge/youtube-white?style=flat&logo=youtube&logoColor=%23000000&labelColor=%23ffffff&color=%23000000"/></a>
    <a href="https://www.tiktok.com/commune_z">
        <img src="https://img.shields.io/badge/tiktok-white?style=flat&logo=tiktok&logoColor=%23000000&labelColor=%23ffffff&color=%23000000"/></a>
    <a href="https://twitter.com/commune_z">
        <img src="https://img.shields.io/badge/twitter-white?style=flat&logo=twitter&logoColor=%23000000&labelColor=%23ffffff&color=%23000000"/></a>
</p>

## 💀 Использование скрипта

1. Выполняем ```git clone https://github.com/MyMaiSan/Telegram-Parser.git```
2. Получаем ```api_id``` и ```api_hash``` с помощью [этого сайта](https://my.telegram.org/auth)
3. Вставляем полученные данные в ```config.ini```
4. Выполняем ```pip install -r requirements.txt```
5. Запускаем ```parser.py```
6. Вставляем пришедший от Telegram код
7. Выбираем чат, участников которого необходимо спарсить

## 🔧 Добавление проспама
```python
count = 0

message = '' #Текст сообщения для проспама
photo = 'photo.png' #Фото для проспама

with open('members.csv') as f:
    reader = csv.reader(f)
    for row in reader:
        if count < 5:
            if row[0] == "":
                pass
            else:
                client.send_file(row[0], photo, caption=message)

            time.sleep(2)
            count += 1

        elif count == 5:
            count = 0
            time.sleep(10)
```
