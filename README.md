Тестовое задание на вакаснию разработчика на Python/Django.
===========================================================

- Язык реализации: `Python 3`.
- Framework: `Django`, с остальными слабо работал или не делал подобные задачи (`Tornado`).
- База данных: `SQLite3`, не вижу зачем может понадобиться большая и функциональная БД, даже `Redis` или `Mongo`.
- Время реализации основного функционала ~ 3.5 часов.

Краткий урл формируется из pk экземпляра модели после вставки строки в БД с преобразованием в 36-ичную систему счисления
или исчисление :D орфография страдает.

Установка
---------

virtualenv .venv --python=python3.4
. .venv/bin/activate
pip install -r requirements.txt
./manage.py syncdb 

Тестовое задание
----------------

Примерное время выполнения - 2-3 часа.

Необходимо написать сервис сокращания ссылок, реализующий следующие возможности:

1. Главная страница, содержащая:
* форму сокращения ссылки;
* 20 самых популярных ссылок в БД (по которым перешли большее количество раз). Ссылки с одинаковым
  количеством просмотров выводятся в порядке убывания "свежести" (добавленные позднее оказываются выше при сортировке).        

2. Страница с постраничным выводом всех добавленных ссылок, отсортированных в порядке убывания
   популярности и "свежести". У каждого элемента списка должна быть ссылка/кнопка, позволяющая его удалить.
      
3. Перенаправление с сокращенной ссылки на ее оригинальную версию.

4. Страница с информацией о ссылке (дата создания, количество переходов). Эта страница
   выводится пользователю после сокращения ссылки.

Основные требования к оформлению:

1. Серверная реализация на Python и фреймворке на выбор: Flask, Django, Tornado.
   Также допустимо использовать различные пакеты с PyPI (например SQLAlchemy).
   Зависимости необходимо зафиксировать в requirents.txt в корне приложения.
2. БД: MySQL, MariaDB, PostgreSQL, Redis, MongoDB.
3. Результат необходимо оформить в виде репозитория на gihtub или bitbucket.
4. Верстка и стилизация не играет значения и не будет учитываться при оценке результата.
