##Размеры экранов

Делаем под три размера:

- до 480 пикселей
- от 480 до 728 пикселей
- более 728 пикселей

###Meta для телефонов

`<meta name="viewport" content="width=device-width,initial-scale=1,user-scalable=1,minimum-scale=1,minimal-ui"/>`

###Название папки с проектом `css-practice-homework`

Помни про структуру папок

```html
css-practice-homework
    css
    less
        components
            /* Файлы с вашим компонентами */
        reset.less
        base.less
        styles.less
    index.html
```

Взять **reset.less** можно [здесь](/OXTraining/MikhailLarchanka/wiki/reset.less)

Если вдруг программа `Koala` сломается, то можно использовать консольную команду:
`lessc styles.less > styles.css`, где ]styles.less] – путь к исходному less-файлу, `styles.css` путь к желаемому css-файлу.

###Возможные компоненты

* header
* footer
* section
* news-item
* gallery-item
* menu
* search
* другие...

###@media

`@media` будем писать не в отдельные файлы, а непосредственно в классы. Пример для `Less`

```less
.class-name {
    background-color: #ff0;

    @media screen and (min-width: 481px) {
        background-color: darken(#ff0, 20%);
    }
}
```

###Переменные в Less

В `base.less` рекомендую написать переменные для цветов и размеров:

```less
@backgroundColor: #fff;
@textColor: #000;
@mainFontSize: 16px;
@h1FontSize: 2em;
/* другие переменные */
```

Помните, что в `less` есть формулы, например:

```less
.class-name {
    font-size: @mainFontSize * 2;
}
````

##Делаем 2 страницы

1. Главная
2. Информационная (страница с новостью)

Обе с одинаковым дизайном, но разной структурой. Соответственно, многие компоненты будут на этих страницах частично одинаковые, например `header`, `menu` и `footer`.

##Размерности

Никаких пикселей, для with блоков используем проценты, для шрифтов и отступов `em`.

##Примеры на занятии

Все что я показывал на занятии можно найти [вот здесь](https://github.com/OXTraining/MikhailLarchanka/tree/master/homework/css-practice).

##Сетка

[Сделал файл `grid.less`](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/grid.less) со стилями для сетки на 12 колонок, но помним, что у нас будет сетка на 6 колонок, соответственно самая тонкая колонка – `col-1-6`. Какие классы существуют, можно прочесть на сайте [Simple Grid](http://thisisdallas.github.io/Simple-Grid/).

##Общий дизайн

Название сайта **Рога и Копыта**.

Логотип в [SVG](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/logo.svg), в [PNG](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/logo.png)

![](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/logo.png)

Максимальная ширина сайта `1140px`, минимальная – `320px`.

На главной странице все разделы должны быть обернуты в тег `section`.

Примерная архитектура главной страницы:

![](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/mainpage.jpg)

Второй ряд меню должен быть только на главной странице и перемещать по якорям на главной странице. Оба меню должны прятаться.

Иконка поиска должна показывать / скрывать форму поиска справа от логотипа. 

![](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/search.png)

Примерная архитектура текстовой/информационной страницы:

![](https://raw.githubusercontent.com/OXTraining/MikhailLarchanka/master/homework/css-practice/newspage.jpg)