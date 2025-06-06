# JWT Authentication App

Простое веб-приложение с аутентификацией на основе JWT токенов.

## Функционал
- Регистрация новых пользователей
- Вход в систему
- Доступ к защищенным данным
- Автоматическая проверка JWT токена
- Хранение пользователей в памяти сервера

## Технологии
- **Бэкенд**: Node.js + Express
- **Аутентификация**: JWT (JSON Web Tokens)
- **Фронтенд**: Чистый HTML/CSS + JavaScript
- **Хранение данных**: In-memory (для демонстрации)

## Установка и запуск

### 1. Клонирование репозитория
```bash
git clone https://github.com/ваш-username/jwt-auth-app.git
cd <папка-проекта>
```
### 2. Установка зависимостей
``` bash
npm init
npm install express jsonwebtoken body-parser cors dotenv
```
### 3. Запуск проекта
```bash
cd backend
node server.js
```
### 4. Сервер будет доступен по адресу: http://localhost:3000

## Использование

### Доступные страницы:
- Главная: http://localhost:3000
- Регистрация: http://localhost:3000/register.html
- Вход: http://localhost:3000/login.html
- Защищенная страница: http://localhost:3000/dashboard.html
### Рабочий процесс:
#### 1. Зарегистрируйте нового пользователя через /register.html
#### 2. Войдите в систему через /login.html
#### 3. После успешного входа вы будете перенаправлены на /dashboard.html
#### 4. Теперь вы можете:
- Обновлять страницу dashboard - доступ сохранится
- Закрыть и снова открыть браузер - доступ сохранится (пока токен действителен)
- Нажать "Logout" для выхода

## Особенности реализации

- Токены действительны 1 час (настраивается в server.js)
- При истечении токена происходит автоматический выход
- Все пользователи хранятся в памяти сервера (исчезают после перезапуска)