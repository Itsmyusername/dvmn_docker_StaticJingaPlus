## Установка и запуск

### Установка Docker
Инструкция по установке Docker - https://docs.docker.com/

### Создание сайтов
Для рендеринга html-шаблонов из шаблонов, запустите из командной строки:

```
sudo docker run -v <path_to_folder>:opt/StaticJinjaPlus/templates -v <path_to_folder>:opt/StaticJinjaPlus/build --rm xofrik/static-jinja-plus
```

Пример вывода в консоль:
```
Rendering about.html...
Rendering assets/style.css...
Rendering faq.html...
Rendering index.html...
```