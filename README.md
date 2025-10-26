# GratitudeApp

gRPC protocal

DOckerfile

FROM node:18-alpine
WORKDIR /app
COPY services/api-gateway/package* ./
RUN npm ci || npm install --production
COPY services/api-gateway/. .
COPY ./protos ./protos
ENV HOST=0.0.0.0
ENV PORT=5000
EXPOSE 5000
CMD [ "node", "index.js" ]  

npm ci because - countinues integration for faster installation with dependencies
|| npm install --production = if npm ci fails, then npm install works; --production because of faster installation
