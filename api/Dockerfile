# Используем официальный образ Node.js в качестве базового
FROM node:18-alpine

# Указываем рабочую директорию в контейнере
WORKDIR /usr/src/app

# Копируем package.json и package-lock.json в контейнер
COPY package*.json ./

# Устанавливаем зависимости
RUN npm install

# Копируем все остальные файлы проекта в контейнер
COPY . .

# Открываем порт, на котором будет работать наше API
EXPOSE 5000

# Устанавливаем команду для запуска API
CMD ["node", "index.mjs"]
