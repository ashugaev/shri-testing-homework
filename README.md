## Коментарии

1. Изначально я начал прокидывать моки в аргументы ф-ции, потом понял, что можно мокнуть модули через "jest.mock()", по этому у меня есть и одна и другая реализация.
1. Из за того, что проверяются достаточно большие куски данных тесты не очень читабельные. Наверное стоило все вынести в один файл с константами.
1. e2e тесты я недонастроил


# Логические блоки/Сценарии

## Навигация (navigation.js)
1. buildFolderUrl 
- Генерация url к папке cо всеми входными данными
- Генерация url к папке без переменной path
2. buildFileUrl  
- Генерация url к файлу
3. buildBreadcrumbs
 - Создание объекта breadcrumbs для главной стр
 - Создание объкета breadcrumbs для всех стр кроме главное

 ## Работа с коммитами (git.js)
 1. executeGit 
 - Инициализация 
 2. parseHistoryItem
 - Преобразование строки с данными о коммите в объект
 3. gitHistory
 - Получение истории коммитов
 4. parseFileTreeItem 
 - преобразование в объект информации о файле
 5. gitFileTree
 - Получение списка файлов
 6. gitFileContent
 - Получение содержимого файла
 7. Вывод списка коммитов (indexContorller.js)
 - Вывод списка коммитов
 - Ошибка вывода
 
 ## Содержимое файла (contentController.js)
 - Генерация содержимого страницы
 - Ошибка вывода

 ## Работа со списком файлов (filesController.js)
 1. builtObjectUrl
 - Генерация ссылки для папки
 - Генерация ссылки для файла
 - При отсутствии типа вернуть #
 2. filesController
 - Вывод содержимого страницы для списка файлов
 - Ошибка вывода

# Запуск/Настройка

## Запуск модульных тестов

```sh
 npm i
 npm test
```

## Запуск интеграционных тестов

! Важно, что бы были установлены драйвера для работы с браузерами, selenium, java, Python(кажется) и все остальное, на что будет ругаться selenium при запуске.

```sh
 npm i
 npm start
  # В отдельной вкладке
 npm run selenium
 # В отдельной вкладке
 npm run hermione
```