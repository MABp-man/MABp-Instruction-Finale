# Работа с ключами SSH для GIT HUB

## Генерация и размещение

1. Команда генерации ключей SSH вводится в терминале:
__*ssh-keygen -t ed25519 -b 4096*__

2. Сгенерированные 2 файла ключей необходимо разместить в папке: __*~/users/USERNAME/.ssh/*__ (где USERNAME = имя пользователя Windows)

3. Открываем файл с расширением __*.pub*__ любым обыкновенным текстовым редактором (например, блокнотом) и копируем всю строку ключа целиком в буфер обмена

4. В своём аккаунте на *__GIT HUB__* в настройках находим пукнт __*SSH and GPG keys*__. Создаём новый ключ SSH и в соответствующее поле вставляет из буфера обмена сгенерированный ключ.

## Привязка к терминалу

Для начала работы с удалённым репозиторием через __*GIT HUB*__ с помощью терминала __*GIT BASH*__ сперва необходимо активировать SSH агента следующими командами:
+ eval "$(ssh-agent -s)"

+ ssh-add ~/.ssh/ssh-key-filename (где *__ssh-key-filename__* = имя файла вашего SSH ключа)
