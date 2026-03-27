# Домашнее задание к занятию 3 «Резервное копирование» - Моськов Максим

### Задание 1.

rsync -avc --delete --exclude='.*/' ~/ /tmp/backup/

![Скриншот Задания 1](img/task_1.png)

### Задание 2.


'''#!/bin/bash

SOURCE="$HOME/"
DEST="/tmp/backup/"

mkdir -p "$DEST"

if rsync -ac --delete --exclude='.*/' "$SOURCE" "$DEST"; then
    logger "Резервное копирование $SOURCE в $DEST завершено УСПЕШНО."
else
    logger "ОШИБКА резервного копирования $SOURCE в $DEST."
fi'''

![Скриншот Задания 1](img/task_2_log.png)

![Скриншот Задания 1](img/task_2_cron.png)
