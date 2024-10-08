﻿# Library_project2
Этот проект представляет собой учебное приложение,
написанное на Java 8 с использованием Spring MVC, Spring Data JPA, Hibernate и Apache Tomcat 9 для развертывания.

Задачи:
1) Переписать Library_project с использованием Hibernate и Spring Data JPA. В вашем
   проекте не должно быть ни одного SQL запроса. Должны быть реализованы
   сущности (@Entity) Книга и Человек, репозитории и сервисы. PersonDAO и
   BookDAO должны быть пустыми и не должны использоваться, вся работа с БД
   через сервисы.
   Новый функционал:
2) Добавить пагинацию для книг.
   Книг может быть много и они могут не помещаться на одной странице в
   браузере. Чтобы решить эту проблему, метод контроллера должен уметь
   выдавать не только все книги разом, но и разбивать выдачу на страницы.
3) Добавить сортировку книг по году. Метод контроллера должен уметь
   выдавать книги в отсортированном порядке.
4) Создать страницу поиска книг. Вводим в поле на странице начальные буквы
   названия книги, получаем полное название книги и имя автора. Также, если
   книга сейчас находится у кого-то, получаем имя этого человека.
5) Добавить автоматическую проверку на то, что человек просрочил возврат
   книги.

Установка и запуск проекта:

1) Для работы с проектом потребуются следующие инструменты:
   - Java 8
   - PostgreSQL 10
   - Apache Tomcat 9
   - IntelliJ IDEA (или другая среда разработки)

2) Клонируйте репозиторий на вашу локальную машину:
   git clone https://github.com/Secamm66/Library_project2.git

3) Установите PostgreSQL 10 и создайте новую базу данных:
   - CREATE DATABASE library_db
   - Создайте таблицы, используя код из файла src/main/sql/library_db.sql
   - Настройте подключение к базе данных в файле src/main/resources/hibernate.properties, заменив значения на ваши собственные

4) Настройте Apache Tomcat 9:
   - Скачайте и установите Apache Tomcat 9 с официального сайта https://tomcat.apache.org
   - Добавьте Tomcat сервер в вашу среду разработки IntelliJ IDEA
   - Откройте IntelliJ IDEA и перейдите в File -> Settings -> Build, Execution, Deployment -> Application Servers
   - Нажмите на + и выберите Tomcat Server, укажите путь до папки с установленным Tomcat
   - В настройках конфигурации запуска проекта добавьте новую конфигурацию для Tomcat
   - Перейдите в Run -> Edit Configurations
   - Нажмите + и выберите Tomcat Server -> Local
   - Выберите ранее добавленный Tomcat и укажите ваш проект как артефакт для деплоя

5) Откройте и запустите проект в IntelliJ IDEA:
   - Убедитесь, что все зависимости и библиотеки установлены корректно (например, для работы с Hibernate и PostgreSQL)
   - Настройте конфигурацию для запуска проекта на Tomcat, как указано в пункте 4
   - Убедитесь, что сервер PostgreSQL запущен
   - Запустите сервер Apache Tomcat из IntelliJ IDEA через созданную конфигурацию
   - Откройте браузер и перейдите по адресу: http://localhost:8080