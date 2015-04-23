Шаблон проекта для быстрого старта (Gulp)
=========================================

В качестве сборщика проекта используется `gulp`


- Stylus
- JS и CoffeeScript (при необходимости)
- Jade (при необходимости)
- Спрайты


## Структура
- `builder` – папка в которой лежит сборщик проекта
     + `builder/gulpfile.js` – основные настройки проекта
- `src` – исходные файлы проекта
     + `src/css` – файлы стилей
     + `src/js` – файлы JS/CoffeScript
     + `src/templates` – jade-шаблоны
- `layout` – HTML и скомпилированные файлы


## Старт проекта

### Установка
Предполагается, что у вас уже установлен `node.js` и пакетные менеджер `npm`.

Перейдите в папку `builder` и выполните команду `npm install`.

### Запуск
Все команды следует выполнять находясь в папке `builder`

- `gulp` – сборка проекта с минификацией js и css
- `gulp debug` – сборка проекта без минификации js и css

Обе команда запускают процесс отслеживания изменений

### Jade
По умолчанию компиляция jade-шаблонов отключена, включить можно в `builder/gulpfile.js

```
    'jade': {
        'enable': true
    }
```
Jade-шаблоны лежат в папке `src/templates`. Компилируются все `*.jade`.

Исключения:

-  содержимое папок `includes`
- `base.jade`