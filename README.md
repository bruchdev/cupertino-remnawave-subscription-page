<p align="center">
     <img src="/assets/page.jpg" height="500">
</p>

# Cupertion Remnawave Subscription Page

Кастомная страница подписки для Remnawave в Apple-like стиле.

## Особенности

- [x] Языки: Русский и Английский
- [x] Темная и светлая тема
- [x] Автоматическое определение языка
- [x] Автоматическое определение темы устройства


## Установка

1. **Скачайте файлы**

   Скачайте файлы `index.html` и `output.css` в ту же папку, где находится ваш `docker-compose.yml`:

     ```bash
     curl -O https://raw.githubusercontent.com/bruch-alex/cupertino-remnawave-subscription-page/refs/heads/main/index.html \
          -O https://raw.githubusercontent.com/bruch-alex/cupertino-remnawave-subscription-page/refs/heads/main/output.css
     ```

2. **Добавление в Docker Compose**

     Добавьте путь скачанных файлов в docker-compose.yml

     ```yaml
     services:
       remnawave-subscription-page:
         image: remnawave/subscription-page:latest
         volumes:
           - ./index.html:/opt/app/frontend/index.html
           - ./output.css:/opt/app/frontend/output.css
     ```

3. **Перезапуск контейнера**

     Для применения изменений перезапустите контейнер Docker:

     ```bash
     docker compose down remnawave-subscription-page && docker compose up -d remnawave-subscription-page
     ```
