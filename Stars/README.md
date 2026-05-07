# Telegram Bot - Stars Seller (24/7)

Бот для продажи Telegram Stars с круглосуточной работой на облачном сервере.

## Быстрое развертывание (Бесплатно/Дешево)

### Вариант 1: Render.com (РЕКОМЕНДУЕТСЯ - Бесплатно)

1. Зайди на https://render.com
2. Нажми "New" → "Web Service"
3. Подключи свой GitHub репозиторий
4. Выбери:
   - Runtime: Python 3.11
   - Build: `pip install -r requirements.txt`
   - Start: `python bot.py`
5. Добавь переменную окружения `BOT_TOKEN`
6. Deploy

### Вариант 2: Railway.app (Бесплатный кредит $5/месяц)

1. Зайди на https://railway.app
2. Нажми "New Project"
3. Выбери "Deploy from GitHub"
4. Подключи репозиторий
5. Добавь переменную `BOT_TOKEN`
6. Deploy автоматически

### Вариант 3: PythonAnywhere (Бесплатно)

1. Зарегистрируйся на https://www.pythonanywhere.com
2. Загрузи файлы через Web interface
3. Создай новый консольный скрипт
4. Запусти `python bot.py`

### Вариант 4: VPS (DigitalOcean - $4/месяц)

1. Создай Droplet (Ubuntu 22.04)
2. SSH подключись
3. Установи:
```bash
sudo apt update
sudo apt install python3 python3-pip screen git
git clone YOUR_REPO_URL
cd Stars
pip install -r requirements.txt
screen -S bot
python bot.py
# Ctrl+A+D для отсоединения
```

## Важные шаги:

### 1. Подготовь файлы для облачного хостинга:

```bash
# Инициализируй Git (если еще нет)
git init
git add .
git commit -m "Initial commit"
```

### 2. Добавь BOT_TOKEN в переменные окружения (НЕ в code!)

На хостинге установи переменную окружения вместо жесткого кода.

### 3. Убедись что banner.jpg находится в репозитории

```bash
git add banner.jpg
```

## Для локальной разработки:

```bash
pip install -r requirements.txt
python bot.py
```

## Структура проекта:

```
Stars/
├── bot.py              # Основной файл бота
├── requirements.txt    # Зависимости Python
├── Procfile           # Для Heroku/Render
├── runtime.txt        # Версия Python
├── banner.jpg         # Баннер бота
├── .env               # Локальные переменные (не коммитить!)
└── .gitignore         # Игнорируемые файлы
```

## Мониторинг 24/7:

На Render/Railway боты работают автоматически и перезагружаются при ошибках.

## Поддержка:

Если возникнут проблемы:
- Проверь логи на хостинге
- Убедись что BOT_TOKEN установлен правильно
- Проверь наличие banner.jpg на сервере
