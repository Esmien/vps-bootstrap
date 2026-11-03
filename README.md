# vps-bootstrap

Публичная точка входа для развёртывания сервера. Секретов здесь нет: скрипт
читает стартовые секреты из файла на самой машине и клонирует приватный
репозиторий по токену.

    curl -fsSL https://raw.githubusercontent.com/Esmien/vps-bootstrap/main/bootstrap.sh | sudo bash

Перед запуском положить `/root/bootstrap.env`:

    GITHUB_TOKEN=...
    SECRETS_KEY=...
    TG_FILE_TOKEN=...
    BOT_TOKEN=...          # необязательно
    FILE_BOT_TOKEN=...     # необязательно
    HERMES_BOT_TOKEN=...   # необязательно
    WEBUI_URL=...

Полный лог: `/var/log/vps-bootstrap.log`.

Канонический исходник живёт в приватном `vps-infra/bootstrap.sh`; сюда он
публикуется скриптом `maintainer/publish_bootstrap.py`.
