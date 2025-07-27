# Сайт для тестов кинооптики и кинокамер

Современный веб-сайт на Next.js для демонстрации тестов кинооптики и кинокамер с тёмной кинематографической темой.

## 🎬 Особенности

- ✨ Тёмная кинематографическая тема
- 🎥 Галерея видео с возможностью лайков
- 📱 Адаптивный дизайн (мобильные устройства и ПК)
- 🎨 Современные анимации и переходы
- ⚡ Быстрая загрузка благодаря Next.js
- 🔗 Интеграция с Instagram

## 🚀 Быстрый старт

### Локальная разработка

```bash
# Установка зависимостей
npm install

# Запуск сервера разработки
npm run dev

# Сборка проекта
npm run build

# Запуск production версии
npm start
```

Откройте [http://localhost:3000](http://localhost:3000) в браузере.

## 📁 Структура проекта

```
vercel/
├── components/          # React компоненты
│   ├── VideoGallery.tsx # Галерея видео с лайками
│   └── InstagramFeed.tsx # Блок Instagram
├── pages/              # Страницы Next.js
│   ├── _app.tsx        # Основное приложение
│   ├── index.tsx       # Главная страница
│   └── api/           # API эндпоинты
│       └── like.ts    # API для лайков
├── styles/            # Стили
│   └── globals.css    # Глобальные стили
├── public/            # Статические файлы
│   ├── favicon.ico    # Иконка сайта
│   ├── favicon.svg    # SVG иконка
│   └── robots.txt     # Для SEO
├── package.json       # Зависимости
├── next.config.js     # Конфигурация Next.js
├── tsconfig.json      # Конфигурация TypeScript
└── .eslintrc.json     # Конфигурация ESLint
```

## 🎬 Добавление новых видео

Для добавления новых тестовых видео отредактируйте массив `videos` в файле `pages/index.tsx`:

```typescript
const videos = [
  { src: 'https://lksrental.site/2.mp4', title: 'Тест 2.mp4' },
  { src: 'https://lksrental.site/999.mp4', title: 'Тест 999.mp4' },
  // Добавьте новые видео здесь
  { src: 'https://lksrental.site/новое-видео.mp4', title: 'Новый тест' },
]
```

## 🌐 Деплой на Vercel

### Способ 1: Через GitHub (рекомендуется)

1. **Создайте аккаунт на Vercel**
   - Зайдите на [vercel.com](https://vercel.com)
   - Войдите через GitHub

2. **Импортируйте проект**
   - Нажмите "New Project"
   - Выберите ваш GitHub репозиторий
   - **ВАЖНО:** Установите Root Directory на `vercel` (не корень репозитория)

3. **Настройка проекта**
   ```
   Framework Preset: Next.js
   Root Directory: vercel
   Build Command: npm run build
   Output Directory: .next
   Install Command: npm install
   ```

4. **Деплой**
   - Нажмите "Deploy"
   - Vercel автоматически соберёт и задеплоит проект

### Способ 2: Через CLI

```bash
# Установите Vercel CLI
npm i -g vercel

# Войдите в аккаунт
vercel login

# Из папки vercel запустите деплой
cd vercel
vercel

# При первом деплое указать:
# - Root directory: ./ (текущая папка vercel)
# - Framework: Next.js
```

### ⚠️ Важные настройки для Vercel

Поскольку проект находится в папке `vercel`, а не в корне репозитория:

1. **Root Directory** должен быть установлен на `vercel`
2. **Build Command**: `npm run build` (оставить по умолчанию)
3. **Output Directory**: `.next` (оставить по умолчанию)
4. **Install Command**: `npm install` (оставить по умолчанию)

## 📱 Адаптивность

Сайт полностью адаптирован для:
- 📱 Мобильные устройства (320px+)
- 📱 Планшеты (768px+)
- 💻 Настольные компьютеры (1024px+)
- 🖥️ Широкие экраны (1200px+)

## 🎨 Кастомизация

### Цветовая схема
Основные цвета можно изменить в `styles/globals.css`:
```css
:root {
  --bg-primary: #181818;
  --bg-secondary: #222;
  --text-primary: #eee;
  --accent: #ff6767;
}
```

### Шрифты
Добавьте Google Fonts в `pages/_app.tsx` или используйте локальные шрифты.

## 🔧 Технологии

- **Next.js 14** - React фреймворк
- **TypeScript** - Типизация
- **CSS-in-JS** - Стилизация (styled-jsx)
- **React Hooks** - Управление состоянием
- **Local Storage** - Хранение лайков
- **Responsive Design** - Адаптивность

## 📞 Поддержка

При возникновении проблем:
1. Проверьте, что используете Node.js 18+
2. Убедитесь в правильной настройке Root Directory в Vercel
3. Проверьте консоль браузера на ошибки
4. Убедитесь, что все зависимости установлены

---

✨ **Готово!** Ваш сайт готов к использованию и деплою на Vercel.