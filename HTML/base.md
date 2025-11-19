# 1. Базовая структура документа

**`<!DOCTYPE html>`**

Объявление типа документа. Говорит браузеру, что перед ним HTML5.
``` HTML
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Мой сайт</title>
</head>
<body>
  ...
</body>
</html>
```
---
**`<html>`**

Корневой элемент HTML-страницы.

**Атрибуты:**

+ `lang` — язык документа (`"ru"`, `"en"`, и т.п.)
``` HTML
<html lang="ru">
  ...
</html>
```
---
**`<head>`**

Служебная часть документа: мета-информация, подключение стилей, скриптов, заголовок вкладки.
``` html
<head>
  <meta charset="UTF-8">
  <title>Название страницы</title>
  <link rel="stylesheet" href="styles.css">
</head>
```
---
**`<body>`**

Основное содержимое страницы, которое видно пользователю.
``` html
<body>
  <h1>Привет, мир!</h1>
  <p>Это мой первый сайт.</p>
</body>
```

# 2. Заголовки и текст

**`<h1>–<h6>`**

Заголовки разных уровней. `h1` — самый важный, `h6` — наименее важный.
``` HTML
<h1>Главный заголовок</h1>
<h2>Подзаголовок</h2>
<h3>Подподзаголовок</h3>
```
---
**`<p>`**

Абзац текста.
``` HTML
<p>Это обычный абзац текста на сайте.</p>
```
---
**`<br>`**

Перенос строки без нового абзаца.
``` HTML
<p>Первая строка<br>Вторая строка</p>
```
---
**`<span>`**

Строчный контейнер без семантики. Используется для выделения части текста, чтобы применить к ней стиль или скрипт.
``` HTML
<p>Это <span class="red">важное</span> слово.</p>
```
---
**`<div>`**

Блочный контейнер без семантики. Используется для группировки элементов.
``` HTML
<div class="card">
  <h2>Заголовок</h2>
  <p>Описание карточки.</p>
</div>
```
# 3. Форматирование текста

**`<strong>`**

Логически важный текст (обычно выделяется жирным).
``` HTML
<p>Это <strong>очень важно</strong> прочитать.</p>
```
---
**`<em>`**

Логически выделенный текст (обычно курсив).
``` HTML
<p>Мне кажется, это <em>интересная</em> идея.</p>
```
---
**`<b>` и `<i>`**

Чисто визуальное выделение: `b` — жирный, `i` — курсив. Без дополнительной семантики.
``` HTML
<p><b>Жирный текст</b> и <i>курсивный текст</i>.</p>
```
---
**`<u>`**

Подчёркнутый текст.
``` HTML
<p>Это <u>подчёркнутый</u> фрагмент.</p>
```
---
**`<small>`**

Мелкий текст, часто для примечаний.
``` HTML
<p>Основной текст.<br><small>* Мелкое примечание.</small></p>
```
---
**`<mark>`**

Выделение текста как маркером.
``` HTML
<p>Запомни: <mark>срок сдачи завтра</mark>.</p>
```

# 4. Ссылки и изображения
**`<a>`**

Гиперссылка.

**Основные атрибуты:**

+ `href` — адрес ссылки
+ `target="_blank"` — открыть в новой вкладке
``` HTML
<a href="https://example.com" target="_blank">Перейти на сайт</a>
```
---
**`<img>`**

Вставка изображения.

**Основные атрибуты:**

+ `src` — путь к изображению
+ `alt` — текстовое описание для доступности и на случай ошибки загрузки
``` HTML
<img src="images/photo.jpg" alt="Описание изображения">
```

# 5. Списки
**`<ul>` и `<li>`**

Ненумерованный список (unordered list) — маркеры.
``` HTML
<ul>
  <li>Пункт 1</li>
  <li>Пункт 2</li>
  <li>Пункт 3</li>
</ul>
```
---
**`<ol>` и `<li>`**

Нумерованный список (ordered list).
``` HTML
<ol>
  <li>Первый шаг</li>
  <li>Второй шаг</li>
  <li>Третий шаг</li>
</ol>
```
---
**`<dl>`, `<dt>`, `<dd>`**

Список определений.
``` HTML
<dl>
  <dt>HTML</dt>
  <dd>Язык разметки гипертекста.</dd>

  <dt>CSS</dt>
  <dd>Язык описания внешнего вида документа.</dd>
</dl>
```

# 6. Таблицы
**`<table>`, `<tr>`, `<th>`, `<td>`**

Создание таблиц.
``` HTML
<table>
  <tr>
    <th>Имя</th>
    <th>Возраст</th>
  </tr>
  <tr>
    <td>Алина</td>
    <td>20</td>
  </tr>
</table>
```
---
**`<thead>`, `<tbody>`, `<tfoot>`**

Логическое разделение таблицы на части.
``` HTML
<table>
  <thead>
    <tr>
      <th>Товар</th>
      <th>Цена</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Худи</td>
      <td>6000 ₽</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Итого</td>
      <td>6000 ₽</td>
    </tr>
  </tfoot>
</table>
```

# 7. Формы
**`<form>`**

Форма для ввода данных пользователем.

**Основные атрибуты:**

+ `action` — адрес, куда отправлять данные
+ `method` — способ отправки (`GET`, `POST`)
``` HTML
<form action="/submit" method="post">
  ...
</form>
```
---
**`<input>`**

Поле ввода.

**Важно:** тип поля задаётся через атрибут `type`.

Примеры:
``` HTML
<input type="text" name="username" placeholder="Имя пользователя">
<input type="password" name="password" placeholder="Пароль">
<input type="email" name="email" placeholder="Email">
<input type="checkbox" name="agree"> Я согласен
<input type="radio" name="gender" value="female"> Женщина
<input type="radio" name="gender" value="male"> Мужчина
<input type="submit" value="Отправить">
```
---
**`<label>`**

Подпись к полю ввода. Нужна для удобства и доступности.
``` HTML
<label for="email">Email:</label>
<input id="email" type="email" name="email">
```
---
**`<textarea>`**

Многострочное поле ввода.
``` HTML
<label for="message">Сообщение:</label>
<textarea id="message" name="message" rows="4" cols="40"></textarea>
```
---
**`<select>` и `<option>`**

Выпадающий список.
``` HTML
<label for="size">Размер:</label>
<select id="size" name="size">
  <option value="s">S</option>
  <option value="m">M</option>
  <option value="l">L</option>
</select>
```
---
**`<button>`**

Кнопка.
``` HTML
<button type="submit">Отправить</button>
<button type="button" onclick="alert('Привет!')">Нажми меня</button>
```

# 8. Семантические теги разметки страницы

Эти теги помогают описать структуру страницы более «человечно» и улучшают SEO и доступность.

<header>

Шапка сайта или секции (логотип, меню, заголовок).

**`<header>`**
``` HTML
  <h1>Мой бренд одежды</h1>
  <nav>...</nav>
</header>
```
---
**`<nav>`**

Блок навигации по сайту.
``` HTML
<nav>
  <a href="#home">Главная</a>
  <a href="#catalog">Каталог</a>
  <a href="#contacts">Контакты</a>
</nav>
```
---
**`<main>`**

Основное содержимое страницы (одно на странице).
``` HTML
<main>
  <h2>Каталог одежды</h2>
  ...
</main>
```
---
**`<section>`**

Секция страницы — логический блок.
``` HTML
<section id="about">
  <h2>О бренде</h2>
  <p>История и философия бренда.</p>
</section>
```
---
**`<article>`**

Самостоятельный кусок контента: статья, пост, карточка товара и т.п.
``` HTML
<article>
  <h2>Новая коллекция</h2>
  <p>Описание коллекции...</p>
</article>
```
---
**`<aside>`**

Боковой блок: дополнительная информация, сайдбар.
``` HTML
<aside>
  <h3>Подписка на новости</h3>
  <form>...</form>
</aside>
```
---

**`<footer>`**

Подвал сайта или секции.
``` HTML
<footer>
  <p>&copy; 2025 Мой бренд</p>
  <a href="/privacy">Политика конфиденциальности</a>
</footer>
```

# 9. Медиа
**`<audio>`**

Вставка аудио.
``` HTML
<audio controls>
  <source src="music.mp3" type="audio/mpeg">
  Ваш браузер не поддерживает аудио.
</audio>
```
---
**`<video>`**

Вставка видео.
``` HTML
<video controls width="640">
  <source src="video.mp4" type="video/mp4">
  Ваш браузер не поддерживает видео.
</video>
```
---
**`<source>`**

Источник для `<audio>`, `<video>`, `<picture>`.
``` HTML
<picture>
  <source srcset="image-large.jpg" media="(min-width: 800px)">
  <img src="image-small.jpg" alt="Пример">
</picture>
```

# 10. Метаданные и служебные теги
**`<meta>`**

Мета-информация документа.
``` HTML
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Магазин концептуальной одежды">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```
---
**`<link>`**

Подключение внешних ресурсов: стили, иконки и т.п.
``` HTML
<link rel="stylesheet" href="styles.css">
<link rel="icon" type="image/png" href="favicon.png">
```
---
**`<style>`**

Встроенные CSS-стили.
``` HTML
<style>
  body {
    font-family: sans-serif;
  }
</style>
```
---
**`<script>`**

Подключение или вставка JavaScript-кода.
``` HTML
<script src="app.js"></script>

<script>
  console.log('Привет из скрипта');
</script>
```

# 11. Прочие полезные теги
**`<hr>`**

Горизонтальная линия (разделитель).
``` HTML
<p>Текст до линии</p>
<hr>
<p>Текст после линии</p>
```
---
**`<code>`**

Короткий фрагмент кода.
``` HTML
<p>Функция называется <code>myFunction()</code>.</p>
```
---
**`<pre>`**

Предформатированный текст (сохраняются пробелы и переносы).
``` HTML
<pre>
  line 1
    line 2 с отступом
</pre>
```
---
**`<figure>` и `<figcaption>`**

Оформление иллюстраций с подписью.
``` HTML
<figure>
  <img src="hoodie.jpg" alt="Худи из коллекции">
  <figcaption>Тяжёлое худи с глубоким капюшоном.</figcaption>
</figure>
```
# 12. Минимальный шаблон HTML-страницы
``` HTML
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Мой первый сайт</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
  <header>
    <h1>Мой бренд одежды</h1>
    <nav>
      <a href="#about">О бренде</a>
      <a href="#catalog">Каталог</a>
      <a href="#contacts">Контакты</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>О бренде</h2>
      <p>Тут будет история бренда.</p>
    </section>

    <section id="catalog">
      <h2>Каталог</h2>
      <article>
        <h3>Худи</h3>
        <p>Тяжёлое плотное худи с глубоким капюшоном.</p>
      </article>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Мой бренд</p>
  </footer>
</body>
</html>
```
