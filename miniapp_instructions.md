# 🌐 Mini App — Инструкция по запуску

## Что это
Веб-приложение внутри Telegram с разделами:
📅 Календарь записи · 📊 Прогресс · 📚 Курсы · 🌬 Практики

---

## Шаг 1 — Загрузить index.html на GitHub Pages (5 мин)

1. Зайди на **github.com** → **New repository**
2. Назови: `psy-miniapp` → сделай **Public** → **Create**
3. Нажми **Add file → Upload files**
4. Загрузи файл `index.html`
5. **Commit changes**

**Включи GitHub Pages:**
1. В репозитории → вкладка **Settings**
2. Слева → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / **(root)** → **Save**

Через 1-2 минуты появится URL вида:
`https://ТВО_ЛОГИН.github.io/psy-miniapp/`

---

## Шаг 2 — Вставить свой Railway URL в index.html

Перед загрузкой открой `index.html` в любом текстовом редакторе,
найди строку (примерно в конце файла):

```js
const API_BASE = 'https://YOUR_RAILWAY_APP.railway.app/api';
```

Замени `YOUR_RAILWAY_APP.railway.app` на реальный URL твоего Railway сервиса.

**Найти URL:** Railway → сервис с ботом → вкладка **Settings** → раздел **Domains**

---

## Шаг 3 — Добавить переменную в Railway

Railway → сервис с ботом → вкладка **Variables** → **New Variable**:

| Name | Value |
|---|---|
| `MINI_APP_URL` | `https://ТВО_ЛОГИН.github.io/psy-miniapp/` |

---

## Шаг 4 — Залить psybot_20 на GitHub

Замени все файлы в репозитории бота на файлы из архива `psybot_20.zip`.
Railway передеплоит автоматически.

---

## Готово!

В боте у клиента появится кнопка **🌐 Личный кабинет** — при нажатии
открывается Mini App прямо внутри Telegram.

---

## Что работает без API (offline/demo режим)

Если API недоступен — Mini App показывает демо-данные:
- Календарь с тестовыми слотами
- График настроения с примерами
- Все практики и курс

Для полноценной работы (реальные слоты, прогресс клиента) нужен рабочий API.
