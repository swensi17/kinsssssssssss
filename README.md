# Кинопоиск клон

Веб-приложение для поиска и просмотра информации о фильмах, построенное с использованием:
- Python Flask
- TMDB API
- HTML/CSS/JavaScript

## Основные функции
- Поиск фильмов
- Просмотр детальной информации о фильмах
- Фильтрация по жанрам
- Просмотр коллекций фильмов
- Информация об актерах

---

## 🌟 Ключевые возможности

### 🎥 Основные функции
- **Умный поиск** с автодополнением и фильтрацией
- **Детализация фильмов**: 
  - Рейтинг TMDB с анимацией
  - Полные метаданные (год, жанры, описание)
  - Актерский состав с фото
- **Трейлеры 4K** с приоритетом русской озвучки
- **Персонализированные рекомендации** на основе AI

### 🎨 Уникальные фишки
```css
/* Интерактивные элементы */
.movie-card {
  transform: scale(1);
  transition: all 0.3s ease;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.movie-card:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 40px rgba(33, 208, 122, 0.2);
}
```
- Анимированные hover-эффекты
- Адаптивная сетка постеров
- Кастомные модальные окна с параллаксом
- Ночной режим (в разработке 🔧)

---

## 🛠 Технологический стек

### Backend
| Технология       | Назначение                     |
|------------------|--------------------------------|
| Python 3.10      | Ядро приложения               |
| Flask 2.0        | Веб-фреймворк                |
| Requests         | Работа с TMDB API            |
| python-dotenv    | Управление переменными среды   |

### Frontend
```html
<!-- Пример компонента -->
<div class="movie-card" data-rating="8.5">
  <div class="rating-badge">
    <i class="fas fa-star"></i>
    <span>8.5</span>
  </div>
</div>
```
- Bootstrap 5 + кастомные стили
- Font Awesome 6 иконки
- YouTube Player API
- Адаптивная верстка

---

## 🚀 Быстрый старт

### Требования
- Python 3.8+
- API ключ TMDB ([получить](https://www.themoviedb.org/documentation/api))

### Установка за 5 минут
1. Клонируйте репозиторий:
```bash
git clone https://github.com/swensi17/FilmoraLands.git && cd FilmoraLands
```

2. Настройте окружение:
```bash
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
```

3. Создайте `.env` файл:
```ini
FLASK_APP=main.py
FLASK_ENV=development
TMDB_API_KEY=ваш_ключ
```

4. Запустите сервер:
```bash
flask run --host=0.0.0.0 --port=5000
```

---

## 🎮 Как пользоваться

### Основные сценарии
1. **Поиск фильмов**  
   Введите название в поисковую строку → получите grid-галерею

2. **Просмотр деталей**  
   Клик на постер →  
   ✔️ Трейлер в HD  
   ✔️ Актерский состав с биографиями  
   ✔️ Полная информация о франшизе

3. **Работа с API**  
Пример запроса к TMDB API:
```python
@app.route('/movie/<int:movie_id>')
def get_movie(movie_id):
    response = requests.get(
        f"{BASE_URL}/movie/{movie_id}",
        params={"api_key": API_KEY, "language": "ru-RU"}
    )
    return render_template('movie.html', movie=response.json())
```

---

## 🛠 Архитектура проекта

```
FilmoraLands/
├── static/
│   ├── css/
│   │   └── style.css       # Кастомные стили
│   └── js/
│       └── script.js       # Интерактивные элементы
├── templates/
│   ├── movie.html          # Детали фильма
│   └── search.html         # Страница поиска
├── main.py                 # Ядро приложения
└── requirements.txt        # Зависимости
```

---

## 📸 Скриншоты

### Главная страница
![Главная страница](https://github.com/swensi17/FilmoraLands/raw/main/static/images/main_page.png)

### Страница поиска
![Страница поиска](https://github.com/swensi17/FilmoraLands/raw/main/static/images/search_page.png)

### Детальная страница фильма
![Детальная страница фильма](https://github.com/swensi17/FilmoraLands/raw/main/static/images/movie_details.png)

### Модальное окно
![Модальное окно](https://github.com/swensi17/FilmoraLands/raw/main/static/images/modal.png)

---

## 🤝 Как помочь проекту

1. Форкните репозиторий
2. Создайте feature-ветку:
```bash
git checkout -b feature/amazing-feature
```
3. Зафиксируйте изменения:
```bash
git commit -m "Добавил крутую фичу"
```
4. Отправьте изменения:
```bash
git push origin feature/amazing-feature
```
5. Создайте Pull Request на GitHub.

## 📜 Лицензия

Этот проект лицензирован под лицензией MIT. Подробности смотрите в [LICENSE](LICENSE).

## 📬 Контакты

Если у вас есть вопросы или предложения, вы можете связаться со мной по следующим каналам:

- **Email:** [ваш_email@example.com](mailto:ваш_email@example.com)
- **GitHub:** [swensi17](https://github.com/swensi17)
- **Telegram:** [swensi17](https://t.me/swensi17)

---

**Спасибо за использование FilmoraLands!**  
Следите за обновлениями и новыми функциями! 🚀
