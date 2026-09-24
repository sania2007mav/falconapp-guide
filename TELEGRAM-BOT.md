# FalconApp — Telegram-бот отчётов

- **Бот:** https://t.me/FalconLogistic_bot (`@FalconLogistic_bot`)
- **Канал отчётов:** https://t.me/+qJ8J_ZgM9Ck4ZGVi (FalconApp)
- **Сайт:** https://falconapp.melnichuk.kz/

## Команды

| Команда | Что присылает |
|---------|----------------|
| `/utro` | Утренний снимок: выручка, клиенты ↑↓, дебиторка, дефицит, мёртвый сток |
| `/mom` | Этот месяц vs прошлый |
| `/top` | Топ клиентов |
| `/dolg` | Дебиторка |
| `/deficit` | Дефицит остатков |
| `/mertvyy` | Мёртвый сток |
| `/sklady` | Сравнение складов |
| `/here` | Привязать текущий чат/канал к рассылке |
| `/help` | Справка |

Авторассылка **`/utro` каждый день в 09:00** (время сервера).

## Подключение канала FalconApp

1. Откройте канал → управление → администраторы.
2. Добавьте **@FalconLogistic_bot** с правом **публиковать сообщения**.
3. Напишите в канале: `/here` или `/utro`.
4. Бот запомнит канал и будет слать туда отчёты.

## Личный чат

Напишите боту `/start`, затем любую команду из таблицы.

## Для администратора (сервер)

Сервис: `falconapp-bot` на CT200.

```powershell
$env:TELEGRAM_BOT_TOKEN = "…"   # токен от @BotFather
python d:\Projects\025MCOMMERCE\falconapp\tools\deploy_telegram_bot.py
```

Разовая отправка:

```bash
cd /opt/falconapp/backend
../venv/bin/python telegram_bot.py send utro
```

Проверка: `systemctl status falconapp-bot`
