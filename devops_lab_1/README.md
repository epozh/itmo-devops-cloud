# Лабораторная работа №1

Выполнила: Пожидаева Елизавета К3244

# Задача лабораторной:

Настроить nginx по заданному тз.

По ТЗ должен работать по https c сертификатом
  1. Настроить принудительное перенаправление HTTP-запросов (порт 80) на HTTPS (порт 443) для обеспечения 
     безопасного соединения.
  2. Использовать alias для создания псевдонимов путей к файлам или каталогам на сервере.
  3. Настроить виртуальные хосты для обслуживания нескольких доменных имен на одном сервере.
  4. Что угодно еще под требования проекта

# Ход работы

1. Обновляем пакетный менеджер:
   ![Снимок экрана от 2024-12-19 20-16-00](https://github.com/user-attachments/assets/e902fc39-226a-4bac-a468-17200b4f4307)

2. Проверяем, что nginx установлен:
   ![Снимок экрана от 2024-10-19 12-29-44](https://github.com/user-attachments/assets/54fe72b4-5491-44bd-b02b-a978745e38c4)

   Создаем сертификат и ключ к нему, чтобы подключиться по https:
   ![Снимок3](https://github.com/user-attachments/assets/efaf817d-26e2-425d-93e9-4a616b5ffa40)

   Создаем файлы project007.com и project700.com, в них прописываем логику перенаправления с 80 на 443 порт, какой сертификат используем для https и корневые папки проектов.
   ![Снимок 4](https://github.com/user-attachments/assets/21a1c6dd-d61a-4677-9020-657d86d775ba)
   ![Снимок 5](https://github.com/user-attachments/assets/dc7d6395-917a-45ac-8add-fc8d65c65a2c)

   Создаем файлы index.html в корневых папках проектов:
   ![Снимок 6](https://github.com/user-attachments/assets/8950104c-da63-49d1-9242-6d9e148d3ac4)
   ![Снимок 7](https://github.com/user-attachments/assets/3d690eda-9a56-43e3-b0dc-8dd17710c854)

   Прописываем в /etc/hosts доменные имена, чтобы они открывались на сервере.
   ![Снимок 8](https://github.com/user-attachments/assets/dff3c2e8-bd15-4cd0-9de9-9a8d100dbe21)

   Пишем в браузере доменные имена проектов и проверяем, открываются ли они и совершается ли переадресация с http на https:
   ![377791977-a95fc0eb-2de9-4b33-aa40-e1df4343c506](https://github.com/user-attachments/assets/ea942140-f29f-4201-8f3a-6842f7a0222b)
   ![2](https://github.com/user-attachments/assets/148c4551-04ab-4e4e-8d95-af4da443426c)
   ![3](https://github.com/user-attachments/assets/65b4d013-82ef-4cd4-8931-ae33ec8ff188)
   ![4](https://github.com/user-attachments/assets/f678a447-0b13-4fd2-87bc-58fd35085119)

3. Прописываем alias в файлах проектов:
   ![Снимок 9](https://github.com/user-attachments/assets/30462b0a-ef4c-4783-8b65-3a308aaa63f7)
   ![Снимок 10](https://github.com/user-attachments/assets/7801096e-ae7a-412a-bbc0-ff0a8631e637)

   Создаем файлы в указанных папках и проверяем в браузере работает ли alias:
   ![11](https://github.com/user-attachments/assets/fd572b8a-952c-4e3e-a2c7-79bcc4ea91c2)
   ![12](https://github.com/user-attachments/assets/4e346412-8b7f-439d-a921-9eb27cb34a9f)

  # Все работает!)
