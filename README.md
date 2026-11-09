# Последний бастион — сборка для теста в браузере

Здесь лежит только готовая WebGL-сборка игры, без исходного кода.
Играть: https://vitto5747.github.io/lastbulwark-play/

Вне Яндекс Игр реклама и облачные сохранения не работают, прогресс хранится в браузере.

## Деплой на cyberti.vorobeyart.ru

Workflow `.github/workflows/deploy-ftp.yml` заливает сборку по FTP при каждом пуше в `main` (или вручную через Actions → Run workflow).
Нужны секреты репозитория: `FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD` и, если сайт лежит не в корне FTP, `FTP_SERVER_DIR` (например `public_html/`).

Индексация закрыта: `robots.txt` (Disallow: /), мета-тег `noindex` в `index.html` и заголовок `X-Robots-Tag` в `.htaccess`.
