FROM node:8-alpine
WORKDIR /app
COPY . .
RUN npm install express
RUN npm install
EXPOSE 8080
CMD ["npm", "start"]