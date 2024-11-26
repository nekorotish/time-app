# Используем базовый образ с Node.js
FROM node:18-alpine

# Устанавливаем рабочую директорию внутри контейнера
WORKDIR /usr/src/app

# Копируем package.json и package-lock.json (если есть)
COPY package*.json ./

# Устанавливаем зависимости внутри контейнера
RUN npm install

# Копируем остальные файлы приложения
COPY . .

# Открываем порт, на котором будет работать приложение
EXPOSE 5050

# Запускаем приложение
CMD ["npm", "run", "preview"]
