# Профосмотр Бот

Telegram-бот: отправляете фото/PDF направления → бот распознаёт данные → присылает Excel.

## Команды
- Фото или PDF — распознать направление и добавить в список
- `/list` — показать все текущие записи
- `/excel` — получить Excel-файл прямо в чат
- `/clear` — очистить список

## Деплой на Railway

### 1. Получить Telegram Token
1. Написать [@BotFather](https://t.me/BotFather) в Telegram
2. Команда `/newbot`, дать имя боту
3. Скопировать токен вида `123456:ABC-DEF...`

### 2. Получить Anthropic API Key
1. Зайти на [console.anthropic.com](https://console.anthropic.com)
2. API Keys → Create Key
3. Скопировать ключ вида `sk-ant-...`

### 3. Деплой на Railway
1. Зайти на [railway.app](https://railway.app) и создать аккаунт
2. New Project → Deploy from GitHub repo (или загрузить папку)
3. В настройках проекта → Variables добавить:
   - `TELEGRAM_TOKEN` = ваш токен от BotFather
   - `ANTHROPIC_API_KEY` = ваш ключ от Anthropic
4. Settings → Service → убедиться что запускается `worker: python bot.py`
5. Deploy!

### 4. Проверка
Написать боту `/start` в Telegram — должен ответить.
