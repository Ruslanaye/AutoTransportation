Создание сайта на языке Java на тему «Автомобильные перевозки. Тарификация и маршруты
Структура проекта
Описание проекта
Проект написан на Java с использованием фреймворка Spring, БД MySQL, а также с помощью HTML и CSS. Структура проекта соответствует схеме MVC. Таким образом, все файлы проекта (за исключением файлов свойств, зависимостей и т.д.) попадают под одну из категорий: models, views, controllers.

Описание сервиса
Сервис организует отправку данных и в дальнейшем ее обработку. На сайте имеется окно регистрации и окно регистрации пользователей. Также в сервисе имеет три роли: администратор, водителей, пользователей. В зависимости от вида роли, каждой из их присущи равные уровни доступа. У пользователя имеется возможность регистрации и отправки заявки на поездку. У водителей имеются права просмотра заявок пользователей и в дальнейшем их обработку(принять/отклонить). У Администратор есть все возможности, которые имеет пользользователь и водитель, но с дополнительными функциями администрирования пользователей(удаление, изменение роли, удаление роли), а также удаление записей бронирования. Заходить на сайт может только авторизованный пользователей.

Models
Сервис работает с базой данных, в которой хранятся данные пользователей, роли, запросы и их темы. Поэтому под категорию моделей попадают все классы данных, хранящихся в БД, репотизориев и сервисов.

Views
Работу сервиса отображают страницы сайта при помощи HTML-документов, которые в свою очередь отображают различную информацию, в зависимости от уровня допступа(роль пользователя, наполнение базы данных и т.д.).

Controllers
Для того, чтобы загружать страницы сайта с нужной информацией, а также для обработки POST запросов нужны классы, которые будут всё это делать. Под эту категорию как раз попадают контроллеры. Они достают из БД нужные данные, а затем отправляют их на страницы, которые их уже отображают нужным образом. Также контроллеры формы на страницах, добавляя в БД новые данные.

Как собрать проект
Чтобы запустить данный проект на своём пк, нужно:

1)Скачать среду разработки Intellij Idea создать Spring Boot проект.
2)Скачать данные проект
3)Открыть в среде Intellij Idea
4)В СУБД MySQL создать базу данных с название auto.
5)Включить локальный сервер, указать номер порта в application.properties и ввести учетную запись, которую будете использовать
6)Запустить проект
7)Заполнить таблицу roles именами привелегий
8)Открыть в браузере и ввести ссылку http://localhost:8090/
