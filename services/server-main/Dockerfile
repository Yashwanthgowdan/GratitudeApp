FROM node:18-alpine
WORKDIR /app
COPY services/server-main/package* ./
RUN npm ci || npm install
CMD ["node", "index.js"]