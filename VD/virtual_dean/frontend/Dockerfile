FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN chmod -R 755 node_modules/.bin
RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "dist", "-l", "3000", "--single"]