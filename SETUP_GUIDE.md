# 🎯 Пошаговая инструкция по настройке сайта

## Шаг 1: Добавление изображений

### Создайте папку images и добавьте:

1. **profile.jpg** - Ваше фото (800x800px)
2. **album1.jpg, album2.jpg, album3.jpg** - Обложки альбомов (1000x1000px)
3. **video1.jpg, video2.jpg, video3.jpg** - Превью видеоклипов (1920x1080px)
4. **merch1.jpg, merch2.jpg, merch3.jpg** - Фото мерча (1000x1000px)

**Где взять изображения:**
- Собственные фото
- [Unsplash](https://unsplash.com) - бесплатные фото
- [Pexels](https://pexels.com) - бесплатные фото
- Создать в [Canva](https://canva.com)

## Шаг 2: Интеграция Яндекс.Музыки

### Подробная инструкция:

1. **Перейдите на Яндекс.Музыку:**
   - Откройте [music.yandex.ru](https://music.yandex.ru)
   - Войдите в свой аккаунт

2. **Найдите свой контент:**
   - Откройте альбом, плейлист или трек
   - Если вы артист, откройте свою страницу артиста

3. **Получите iframe код:**
   - Нажмите на три точки (⋮) рядом с названием
   - Выберите "Поделиться"
   - Нажмите "HTML-код" или "Встроить"
   - Скопируйте весь iframe код

4. **Вставьте код в сайт:**

   Откройте файл `index.html`

   Найдите строку 176-179:
   ```html
   <div id="yandex-music-player" class="music-player-placeholder">
       <p>Здесь будет плеер Яндекс.Музыки</p>
       <p class="hint">Вставьте свой iframe код от Яндекс.Музыки</p>
   </div>
   ```

   Замените на:
   ```html
   <div id="yandex-music-player">
       <!-- Вставьте сюда ваш iframe код -->
       <iframe frameborder="0" style="border:none;width:100%;height:450px;"
               width="100%" height="450"
               src="https://music.yandex.ru/iframe/...ВАШ_КОД...">
       </iframe>
   </div>
   ```

### Пример готового кода:

```html
<div id="yandex-music-player">
    <iframe frameborder="0" style="border:none;width:100%;height:450px;"
            width="100%" height="450"
            src="https://music.yandex.ru/iframe/playlist/username/1001">
    </iframe>
</div>
```

## Шаг 3: Замена текста и информации

### В файле `index.html` найдите и замените:

#### 1. Логотип (строка 16):
```html
<a href="#home">ВАШ ЛОГОТИП</a>
```

#### 2. Главный заголовок (строка 39):
```html
<h1 class="hero-title fade-in">ВАШЕ ИМЯ</h1>
```

#### 3. Подзаголовок (строка 40):
```html
<p class="hero-subtitle fade-in-delay">Музыкант • Саунд-продюсер • Певец</p>
```

#### 4. Ссылки соцсетей (строки 46-78):

**YouTube:**
```html
<a href="https://youtube.com/@ваш_канал" target="_blank" aria-label="YouTube">
```

**VK:**
```html
<a href="https://vk.com/ваш_id" target="_blank" aria-label="VK">
```

**Telegram:**
```html
<a href="https://t.me/ваш_username" target="_blank" aria-label="Telegram">
```

**Instagram:**
```html
<a href="https://instagram.com/ваш_username" target="_blank" aria-label="Instagram">
```

**Spotify:**
```html
<a href="https://open.spotify.com/artist/ваш_id" target="_blank" aria-label="Spotify">
```

#### 5. Секция "Обо мне" (строки 92-121):

Замените текст в параграфах:
```html
<p>
    Создаю музыку, которая трогает души... ВАШЕ ОПИСАНИЕ
</p>
```

Обновите статистику:
```html
<div class="stat-number">500+</div>  <!-- Количество треков -->
<div class="stat-number">50+</div>   <!-- Количество концертов -->
<div class="stat-number">10M+</div>  <!-- Прослушивания -->
```

#### 6. Альбомы (строки 183-235):

Для каждого альбома обновите:
```html
<h4>Название вашего альбома</h4>
<p>2025</p>  <!-- Год выпуска -->
<div class="streaming-links">
    <a href="ССЫЛКА_SPOTIFY" target="_blank">Spotify</a>
    <a href="ССЫЛКА_APPLE" target="_blank">Apple Music</a>
    <a href="ССЫЛКА_ЯНДЕКС" target="_blank">Яндекс</a>
</div>
```

#### 7. Концерты (строки 297-336):

Обновите даты и места:
```html
<div class="concert-date">
    <span class="day">15</span>
    <span class="month">ЯНВ</span>
</div>
<div class="concert-info">
    <h3>Название клуба/площадки</h3>
    <p>Москва, Россия</p>
</div>
<div class="concert-action">
    <a href="https://ссылка_на_билеты" class="btn btn-primary">Купить билет</a>
</div>
```

#### 8. Контакты (строки 404-425):

```html
<a href="mailto:ваш@email.com">ваш@email.com</a>
<a href="tel:+79999999999">+7 (999) 999-99-99</a>
<a href="https://t.me/ваш_username" target="_blank">@ваш_username</a>
```

## Шаг 4: Настройка цветов

Откройте файл `css/style.css` (строки 7-14):

```css
:root {
    --primary-color: #00ff88;      /* Измените на ваш основной цвет */
    --secondary-color: #ff0080;     /* Измените на ваш вторичный цвет */
}
```

**Популярные цветовые схемы для музыкантов:**

```css
/* Неоновый синий/розовый */
--primary-color: #00d9ff;
--secondary-color: #ff006e;

/* Золотой/фиолетовый */
--primary-color: #ffd700;
--secondary-color: #9d00ff;

/* Зеленый/оранжевый */
--primary-color: #00ff88;
--secondary-color: #ff6b00;

/* Красный/синий */
--primary-color: #ff0055;
--secondary-color: #0099ff;
```

## Шаг 5: Добавление своих альбомов

### Копируйте этот блок для каждого нового альбома:

```html
<div class="album-card">
    <div class="album-cover">
        <img src="images/album4.jpg" alt="Название альбома">
        <div class="album-overlay">
            <button class="play-btn">▶</button>
        </div>
    </div>
    <h4>Название альбома</h4>
    <p>Год</p>
    <div class="streaming-links">
        <a href="#" target="_blank">Spotify</a>
        <a href="#" target="_blank">Apple Music</a>
        <a href="#" target="_blank">Яндекс</a>
    </div>
</div>
```

## Шаг 6: Добавление видео

### Для каждого видео используйте:

```html
<div class="video-card">
    <div class="video-thumbnail">
        <img src="images/video4.jpg" alt="Название трека">
        <div class="video-overlay">
            <button class="play-btn" onclick="window.open('https://youtube.com/watch?v=VIDEO_ID')">▶</button>
        </div>
    </div>
    <h4>Название трека</h4>
    <p>Режиссер: Имя Фамилия</p>
</div>
```

## Шаг 7: Настройка формы обратной связи

### Вариант 1: Email через сервис (рекомендуется)

Используйте [Formspree](https://formspree.io):

1. Зарегистрируйтесь на formspree.io
2. Получите endpoint URL
3. Замените в `index.html` (строка 433):

```html
<form id="contactForm" action="https://formspree.io/f/ВАШ_ID" method="POST">
```

### Вариант 2: Telegram бот

В файле `js/script.js` (строка 78-95) замените на:

```javascript
contactForm.addEventListener('submit', async (e) => {
    e.preventDefault();

    const name = e.target[0].value;
    const email = e.target[1].value;
    const message = e.target[2].value;

    const telegramBotToken = 'ВАШ_ТОКЕН_БОТА';
    const telegramChatId = 'ВАШ_CHAT_ID';
    const text = `Новое сообщение с сайта:\n\nИмя: ${name}\nEmail: ${email}\nСообщение: ${message}`;

    await fetch(`https://api.telegram.org/bot${telegramBotToken}/sendMessage`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ chat_id: telegramChatId, text: text })
    });

    alert('Спасибо! Сообщение отправлено.');
    contactForm.reset();
});
```

## Шаг 8: Тестирование

### Проверьте сайт на разных устройствах:

1. **Desktop** - откройте в браузере
2. **Mobile** - откройте DevTools (F12) → Toggle Device Toolbar
3. **Tablet** - проверьте планшетную версию

### Проверьте все ссылки:
- ✅ Социальные сети открываются
- ✅ Яндекс.Музыка плеер работает
- ✅ Форма отправляется
- ✅ Все изображения загружаются

## Шаг 9: Публикация сайта

### Вариант 1: GitHub Pages (бесплатно)

1. Создайте аккаунт на [github.com](https://github.com)
2. Создайте новый репозиторий с названием `yourname.github.io`
3. Загрузите все файлы
4. В настройках включите GitHub Pages
5. Сайт будет доступен по адресу: `https://yourname.github.io`

### Вариант 2: Netlify (бесплатно)

1. Зарегистрируйтесь на [netlify.com](https://netlify.com)
2. Перетащите папку `website` на сайт
3. Получите ссылку типа `yourname.netlify.app`
4. Можете подключить свой домен

### Вариант 3: Свой домен

1. Купите домен на [reg.ru](https://reg.ru) или [nic.ru](https://nic.ru)
2. Загрузите файлы на хостинг через FTP
3. Настройте DNS

## Шаг 10: SEO оптимизация

### Добавьте в `<head>` секцию `index.html`:

```html
<!-- SEO Meta Tags -->
<meta name="description" content="ВАШЕ ИМЯ - музыкант, саунд-продюсер, певец. Слушай новые треки, смотри видео и узнай о концертах.">
<meta name="keywords" content="ваше имя, музыкант, продюсер, музыка, треки">
<meta name="author" content="ВАШЕ ИМЯ">

<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://ваш-сайт.com/">
<meta property="og:title" content="ВАШЕ ИМЯ | Музыкант & Саунд-продюсер">
<meta property="og:description" content="Официальный сайт">
<meta property="og:image" content="https://ваш-сайт.com/images/profile.jpg">

<!-- Twitter -->
<meta property="twitter:card" content="summary_large_image">
<meta property="twitter:url" content="https://ваш-сайт.com/">
<meta property="twitter:title" content="ВАШЕ ИМЯ | Музыкант">
<meta property="twitter:description" content="Официальный сайт">
<meta property="twitter:image" content="https://ваш-сайт.com/images/profile.jpg">
```

## 🎉 Готово!

Ваш сайт готов к использованию!

**Дополнительные ресурсы:**
- [Google Analytics](https://analytics.google.com) - статистика посещений
- [Google Search Console](https://search.google.com/search-console) - индексация в Google
- [Яндекс.Метрика](https://metrika.yandex.ru) - аналитика

---

**Нужна помощь?** Проверьте консоль браузера (F12) для поиска ошибок.
