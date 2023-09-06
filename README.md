# Космический Телеграм
Этот проект создан для того, чтобы вы могли скачивать и отправлять в телеграм канал космические фотки, которые публикуют такие известные компании, как SpaceX и NASA

## Как установить
Вам понадобятся несколько ключей для этого проекта, например:

1. NASA-токен

    Чтобы получить токен NASA, Вам нужно зайти на их [официальный сайт](https://api.nasa.gov/), перейти в отдел Generate API Key и заполнить небольшую анкету, вы получите токен NASA.

    Вот пример такого токена: `cNSCStK2LflLY8dWT6YJYHkbDtyry3bk0nGy76qW` 

    Когда вы его получите, положите его в `.env`, в формате:

    ```
    NASA_TOKEN = (ВАШ ТОКЕН)
    ```

        
2. Телеграм-бот токен

    Чтобы получить телеграм-бот токен, ознакомьтесь с [этим сайтом](https://parsemachine.com/articles/gde-najti-token-bota-telegram-api/)

    Вот пример такого токена: `123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11 `

    Когда вы его получите, положите его в `.env`, в формате:

    ```
    TELEGRAM_BOT_TOKEN = (ВАШ ТОКЕН)
    ```


3. Телеграм чат-ID

    Чтобы получить телеграм чат-ID, ознакомьтесь с [этим сайтом](https://lumpics.ru/how-find-out-chat-id-in-telegram/)
    Вот пример такого ID в телеграм-каналах: `@che_watch`

    И вот пример такого ID в телеграм-чатах: `5824972924`

    Когда вы его получите, положите его в `.env`, в формате:

    ```
    TELEGRAM_CHAT_ID = (ВАШ ЧАТ-ID)
    ```


Python3 должен быть уже установлен. Затем используйте `pip` (или `pip3`, есть есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```

И вот вы уже можете запустить этот проект!


## Примеры запуска скриптов
1. 
    Вот пример для того, чтобы скачать фотки SpaceX:
    ```
    python download_spacex_pictures.py
    ```
2. 
    Пример для того, чтобы скачать фотки NASA_APOD:
    ```
    python download_nasa_apod_pictures.py
    ```
3. 
    Пример для того, чтобы скачать фотки NASA_EPIC:
    ```
    python download_nasa_epic_pictures.py
    ```
4. 
    Пример для того, чтобы публиковать одну фотку(Или одну из любой папки на Ваш выбор, или вообще любую картинку на Ваш выбор):
    ```
    python send_one_of_all_photo.py
    ```
5. 
    Пример для того, чтобы публиковать все фотки в бесконечном цикле :
    ```
    python send_all_photos.py
    ```
## Дополнение 
Также, есть несколько необязательных дополнений, чтобы улучшить функционал проекта, чтобы узнать их, просто напишите в командной строке:
```
python send_all_photos.py(Любое название файла) --help
```
И если в этом файле есть что-нибудь, что Вы можете дополнить, то там будет выдан текст, например:
```
--time TIME  время между отправкой картинок в секундах
```
И тогда, вы можете написать в командной строке:
```
python send_all_photos.py(Любое название файла) --time(любое дополнение) 4(любое его значение)
```
Это необязательно!
## Цель проекта
Код написан в образовательных целях на онлайн-курсе для веб-разработчиков [dvmn.org](https://dvmn.org/).