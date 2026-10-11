FROM node:20
WORKDIR /app
COPY package*.json ./
RUN npm config set fetch-timeout 600000 && npm config set fetch-retries 5 && npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "run", "start"]