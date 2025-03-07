# Лабораторная работа №3

## Задание:
1. Написать “плохой” CI/CD файл, который работает, но в нем есть не менее пяти “bad practices” по написанию CI/CD
2. Написать “хороший” CI/CD, в котором эти плохие практики исправлены
3. В Readme описать каждую из плохих практик в плохом файле, почему она плохая и как в хорошем она была исправлена, как исправление повлияло на результат
4. Прочитать историю про Васю (она быстрая, забавная и того стоит): https://habr.com/ru/articles/689234/

## Плохой CI/CD файл
![bad_practice](https://github.com/user-attachments/assets/3a5bc67e-4c5e-45fd-a98f-e4aa642c392e)


### Файл запускается:
![bad_practice_test](https://github.com/user-attachments/assets/8e3712b8-e6ea-4b1a-b922-c45afc64988e)

####  Плохие практики:
1.  Использование ubuntu-latest

Ubuntu-latest может обновляться и будут проблемы с совместимостью.

2. Устаревшая версия checkout

Используется устаревшая v1 версия actions/checkout. Последняя стабильная версия — v4.

3. Установка nodejs и npm через apt-get

GitHub Actions уже включает Node.js — нет необходимости устанавливать его вручную. Установка через apt-get может привести к устаревшей версии Node.js.

4. Отсутствие таймаутов

Переход в sleep 5 может привести к неэффективности, особенно если это занимает много времени.


## Хороший CI/CD файл
![good_practice](https://github.com/user-attachments/assets/4e7ca064-997b-45b0-b7f7-adbea50d4289)

### Файл запускается:
![good_practice_test](https://github.com/user-attachments/assets/0f953253-7f2e-4de7-8a17-bc72fe953eb3)


#### Решение проблемы плохих практик:
1. Использование ubuntu-latest

Заменить ubuntu-latest на конкретную версию ubuntu-22.04, чтобы избежать возможных проблем с изменениями в будущих версиях ubuntu-latest.

2.  Устаревшая версия checkout

Обновить до v4

3.  Установка nodejs и npm через apt-get

 Использовать actions/setup-node
 
4.  Отсутствие таймаутов
 Заменить sleep 5 на установку таймаута для выполнения команд

## ВСЕ!
P.S. Интересная история про Васю)
