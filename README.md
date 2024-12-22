# README

# Опис бота
Цей бот призначений для виконання різноманітних завдань, включаючи:
1. Розпізнавання мовлення (STT): Бот може приймати голосові повідомлення та перетворювати їх на текст за допомогою функції розпізнавання мовлення. Для цього використовується модель штучного інтелекту, яка завантажується при першому запуску команди.

## Призначення
Бот створений для полегшення повсякденних завдань, надання інформації та розваг користувачам. Він може бути корисним для тих, хто хоче виконати розпізнавання мовлення або скористатися іншими корисними функціями без необхідності переходити на інші платформи оплачуючи їх.

## Встановлення та активація

1. Клонуйте репозиторій:
   ```
   git clone <URL_вашого_репозиторію>
   cd <назва_папки>
   ```

2. Встановіть необхідні бібліотеки:
   ```
   pip install -r requirements.txt
   ```

3. У файлі `config.py` вкажіть ваші дані для авторизації в Telegram.
API_ID - ID API для Telegram
API_HASH - Hash API для Telegram
PHONE_NUMBER - Номер телефону для авторизації в Telegram

Їх можна отримати на сайті [my.telegram.org](https://my.telegram.org)

4. Запустіть бот:
   ```
   python main.py
   ```

## Використання команд

`$stt` - Розпізнавання мовлення. (Не протестовано на дистрибутивах Linux та MacOS)
`$ping` - Перевірка доступності бота виводячи інформацію про сервер.
`$cat` - Відправка випадкових зображень котів. [Вимагає API ключа для доступу до сервісу](https://thecatapi.com/) (API ключ вказати в конфігураційному файлі)
`$sping` - Перевірка доступності сервера.
`$speedtest` - Виконання тесту швидкості інтернет-з'єднання.
`$8ball` - Відповіді на запитання у стилі "магічної кулі".
`$tracert` - Виконання трасування маршруту до сервера.
`$calc` - Виконання простих математичних обчислень. (працює нестабільно)
`$screen` - Відправка скріншота з екрану (не працює без графічного інтерфейсу)
`$lock` - Блокування екрану.
`$sleep` - Перехід в режим спячого режиму.
`$hibernate` - Перехід в режим гібернації.
`$spotify` - Запускає Spotify та автоматично відтворює останню пісню.

## Використання команди stt

1. Перед використанням команди `stt`, будь ласка, вручну скачайте ffmpeg версії 8.0 і більше та встановіть в папку `packages/ffmpeg/bin/ffmpeg.exe`.

2. Переконайтеся, папка названа `ffmpeg` і знаходиться в папку `packages`.

3. При першому виконанні команди бот буде завантажувати ШІ модель, що може зайняти деякий час.

## Мінімальні характеристики для STT

- Процесор: Intel i7-11 покоління або AMD Ryzen 5 3600
- Оперативна пам'ять: 16 ГБ
- Місце на диску: 5 ГБ

## Рекомендовані характеристики

- Процесор: Intel i9-11 покоління або AMD Ryzen 7 5800X
- Оперативна пам'ять: 32 ГБ
- Місце на диску: 5 ГБ
- Відеокарта: NVIDIA GeForce RTX 3060 або AMD Radeon RX 6700 XT

## Налаштування STT
У конфігураційному файлі `config.py` можна налаштувати параметри для STT.

- `whisper_presets`: Підтримується: `accurate`, `fast`, `normal`, `custom`.

`accurate` - найбільш точний, але і найповільний.
`fast` - найшвидший, але і найменш точний.
`normal` - змішаний режим, який намагається бути точним і швидким.
`custom` - користувацький режим, який дозволяє налаштувати параметри Whisper.

- `beam_size`: Використовується для керування кількістю варіантів, які Whisper буде розглядати.
- `best_of`: Використовується для керування кількістю варіантів, які Whisper буде розглядати.
- `temperature`: Використовується для керування випадковістю результату.

### Ліцензія
Цей проект розповсюджується на умовах ліцензії MIT.
Посилання на ліцензію: [LICENSE](LICENSE)

## Автор
Цей проект створений та підтримується [@fruin_studios](https://t.me/fruin_studios)
Батько бота - [@nestor_churin](https://t.me/nestor_churin)
