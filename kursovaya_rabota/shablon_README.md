# Белая линия — сайт и сквозная аналитика записей

Курсовая работа по дисциплине ОП.03 «Информационные технологии», ТЗ № ТЗ-04/2026.
Исполнитель: Константинов Валерий Владимирович, группа РПО 25/9/3.

Сайт акции «Профессиональная гигиена и консультация за 3 900 ₽»: посетитель приходит с меткой источника, заявка попадает в Google Таблицу, а на дашборде Looker Studio видно, какой канал привёл сеанс.

Схему `docs/scheme.png` в репозиторий проекта ещё нужно положить. Пока путь такой: соцсети и QR → сайт на Vercel → GA4 и Google Таблица → Looker Studio. Кнопка из Direct ManyChat ведёт на тот же сайт.

## Ссылки

| Что | Ссылка |
|---|---|
| Сайт | https://white-line-sooty.vercel.app |
| Таблица заявок | https://docs.google.com/spreadsheets/d/1waEp18y3RePuCvSOQ4wpzFmeiah_zrHQ--enouP6oAk |
| Дашборд Looker Studio | https://lookerstudio.google.com/reporting/a5e677dc-d5a7-4691-b0ec-a3b9651745bc |
| Instagram и автоответ | https://www.instagram.com/noearhiviste/ · «ЧЕК» https://www.instagram.com/p/DfFvPExo1Wi/ · «ДЕТИ» https://www.instagram.com/p/DfFvj4ZITQt/ |
| ВКонтакте · Telegram · YouTube | https://clck.ru/3WkxBN · https://clck.ru/3WkxBP · https://white-line-sooty.vercel.app/checkup.html?utm_source=youtube&utm_medium=social&utm_campaign=hygiene_nov_2026&utm_content=shorts_brushing |
| Описание работы | [docs/opisanie.md](docs/opisanie.md) |
| Презентация к защите | [presentation/zashchita.pdf](presentation/zashchita.pdf) |

Ресурс GA4: `G-7BTPH14B6G`. В GA4 доступ только по почте, ссылки «для всех» нет: Viewer не выдан. Таблица и отчёт Looker Studio открыты всем, у кого есть ссылка, с правом читателя.

Описание и презентация в репозитории проекта ещё не лежат. Готовый текст — в папке `kursovaya_rabota` репозитория `funnel-project`.

## Что сделано

| Часть | Результат |
|---|---|
| Сайт | 8 страниц и `404.html`, статический HTML, Vercel, Lighthouse мобильный: 76 / 95 / 100 |
| GA4 | 20 событий (6 автоматических и 14 своих), 7 пользовательских параметров, ключевые: `generate_lead`, `contact_click`, `messenger_click` |
| UTM | 12 ссылок в реестре, два поста Instagram, размеченные ссылки ВКонтакте, Telegram и YouTube, QR на листовку |
| Заявки | форма → Apps Script → лист `leads`, проверка полей и повторов |
| Instagram | ManyChat, две автоматизации: `ЧЕК` и `ДЕТИ` |
| Отчёты | три исследования GA4 (кампания, воронка, путь) и отчёт Looker Studio из трёх страниц |

## Технологии

HTML, CSS, JavaScript · Google Analytics 4 · Google Таблицы и Apps Script ·
ManyChat · Looker Studio · GitHub и Vercel. Сайт создан с помощью Cursor
(запросы — в [docs/prompts.md](docs/prompts.md)).

## Структура

```text
index.html …         страницы сайта
js/analytics.js      все события GA4
apps-script/Code.gs  приёмник заявок
docs/                реестр UTM, события, записка, журнал запросов
screens/             кадры GA4, Looker Studio, Lighthouse, источники
```

## Итог

Не получилось: отдельные страницы ВКонтакте, Telegram и YouTube; учебный Instagram вместо belaya_liniya_dent; разные ответы на одном посте; кадр самого комментария под постом; ники партнёров; доступ Viewer в GA4 по почте; HubSpot. Проверка кнопок со второго аккаунта есть. Таблица и Looker Studio открыты по ссылке для читателя.

Нейросеть использовалась для: структуры сайта, текстов, вёрстки, портретов врачей, PDF, QR и журнала запросов.
