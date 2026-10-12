# Beowulf: відкритий телемедичний комплект / Open Telemedicine Kit

Сайт студентського конкурсу. Статичний HTML + CSS, без фреймворків і збирання —
публікується на GitHub Pages з гілки `main` (корінь репозиторію).

- `index.html` — українська версія
- `en/index.html` — English version
- `assets/css/styles.css` — спільні стилі (світла й темна теми)
- `assets/img/` — favicon, схема архітектури (UA/EN), Open Graph-зображення
- `.nojekyll` — вимикає обробку Jekyll на GitHub Pages

## Локальний перегляд

```sh
python -m http.server 8080
# відкрити http://localhost:8080/
```

## Заглушки, які треба замінити перед публікацією

Знайти все одразу:

```sh
grep -rn "\[.*\]" index.html en/index.html
```

| Заглушка | Де | Що вписати |
| --- | --- | --- |
| `[посилання на Google Form]` | обидві сторінки, 2 місця на кожній | URL форми заявки |
| `[повна назва OHIN]` / `[full name of OHIN]` | шапка обох сторінок | повна назва організації OHIN |
| `[e-mail]` | розділ контактів | e-mail координатора |
| `[телефон / Telegram]` | розділ контактів | телефон або Telegram |
| `[посилання на документацію API]` | розділ API | URL документації API МІС (після публікації) |

Після заміни видаліть блоки `.todo` з обох сторінок.

## Публікація

GitHub Pages: Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
