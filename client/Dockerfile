FROM node:18-alpine
WORKDIR /app
COPY ./package* ./
RUN npm install || npm ci
COPY . .
EXPOSE 3000
CMD ["npm", "start"]