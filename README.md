# Карты подскажут — Адаптивный лендинг с переключением тем

**Современный адаптивный лендинг с системой переключения светлой и тёмной темы**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/ru/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/ru/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/ru/docs/Web/JavaScript)
[![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://figma.com)

---

## 📖 О проекте

Я разработала адаптивный лендинг "Карты подскажут" с продвинутой системой переключения цветовых тем. Проект демонстрирует современные подходы к веб-разработке, включая использование CSS-переменных, семантической верстки и адаптивного дизайна.

### 🎯 Ключевые особенности

- **Динамическое переключение тем** (светлая/тёмная) с сохранением выбора пользователя
- **Адаптивный дизайн** с использованием относительных единиц измерения
- **Семантическая верстка** с применением современных HTML5-тегов
- **CSS-переменные** для управления цветовой схемой
- **Оптимизированные изображения** в форматах WebP и AVIF
- **Доступность** (WCAG 2.1) и keyboard navigation

### 🛠 Технологический стек

**Frontend:**
- HTML5 (семантическая разметка)
- CSS3 (Grid, Flexbox, CSS Variables, Media Queries)
- Vanilla JavaScript (ES6+)

**Особенности реализации:**
- CSS Custom Properties для динамического изменения тем
- Методология БЭМ для именования классов
- Абсолютное и относительное позиционирование
- Псевдоэлементы для декоративных элементов
- Функция clamp() для резиновой типографики

---

## 🚀 Быстрый старт

### Посмотреть онлайн

🌐 **[Живая демо-версия](https://cutevil-magal.github.io/third-project/)**

### Запуск локально

1. **Клонирование репозитория**
   ```bash
   git clone https://github.com/cutevil-magal/third-project.git
   cd third-project
   ```

2. **Запуск проекта**
   - Откройте файл `index.html` в браузере
   - Для разработки рекомендуется использовать Live Server

### Системные требования
- Современный браузер с поддержкой CSS Variables и ES6+
- Разрешение экрана не менее 320px
- Включенный JavaScript для работы переключателя тем

---

## 📁 Структура проекта

```
third-project/
├── index.html              # Главная страница
├── styles/
│   ├── style.css           # Основные стили
│   └── fonts.css           # Подключение шрифтов
├── fonts/                  # Локальные шрифты
├── images/                 # Изображения (WebP, AVIF)
├── scripts/
│   └── script.js           # Логика переключения тем
└── README.md               # Документация
```

---

## 🎨 Особенности реализации

### Система CSS-переменных
```css
:root {
  --bg-color: #fff;
  --text-color: #000;
  --accent-color: #000;
  --main-font: 'Raleway', sans-serif;
  --accent-font: 'EB Garamond', serif;
}

.theme_dark {
  --bg-color: #000;
  --text-color: #f1f1f1;
  --accent-color: transparent;
}
```

### Адаптивная типографика
```css
.header__title {
  font-size: clamp(7.25rem, 7.0115rem + 1.0178vw, 7.5rem);
  line-height: 82.5%;
}
```

### Семантическая разметка
```html
<main class="content">
  <section class="content-section">
    <h2 class="content__title heading">Дебют</h2>
    <div class="content__text-block content__text-block_type_first-lettered">
      <p class="content__paragraph">...</p>
    </div>
  </section>
</main>
```

### Переключатель тем
```javascript
const themeButton = document.querySelector('.header__theme-button');
themeButton.addEventListener('click', () => {
  document.body.classList.toggle('theme_dark');
  localStorage.setItem('theme', document.body.classList.contains('theme_dark') ? 'dark' : 'light');
});
```

---

## 🎯 Результаты реализации

**Достигнутые цели:**
- ✅ Полное соответствие макету Figma в обеих темах
- ✅ Кроссбраузерная совместимость
- ✅ Сохранение выбора темы пользователя
- ✅ Адаптивность для мобильных устройств
- ✅ Оптимизированная производительность загрузки

**Технические преимущества:**
- Чистая семантическая верстка
- Использование современных CSS-технологий
- Оптимизированные медиа-запросы
- Плавные переходы между темами
- Доступность для screen readers

---

## 🔮 Планы по развитию

- [ ] Добавить дополнительные цветовые схемы
- [ ] Реализовать системные предпочтения темы (prefers-color-scheme)
- [ ] Добавить анимации перехода между темами
- [ ] Оптимизировать загрузку изображений для разных тем
- [ ] Реализовать PWA-функциональность
- [ ] Добавить режим высокой контрастности

---

## 👩‍💻 Разработчик

**Анна Хвостикова** - Frontend Developer

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/cutevil-magal)
[![Email](https://img.shields.io/badge/Email-ana.magal@yandex.by-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ana.magal@yandex.by)

---

## 📄 Лицензия

Проект создан на основе дизайн-макета из Figma. Исходный код доступен для ознакомления и обучения.

**Макет в Figma:** [Ссылка на дизайн](https://www.figma.com/design/4qb9fmrx7bwxFmo7geqzxC/%235-%D0%9A%D0%B0%D1%80%D1%82%D1%8B-%D0%BF%D0%BE%D0%B4%D1%81%D0%BA%D0%B0%D0%B6%D1%83%D1%82?node-id=0-1&t=lRI10Gb33o5kQFHa-1)

---
