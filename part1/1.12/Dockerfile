FROM node:16.14.0

WORKDIR /usr/src/app

EXPOSE 5000

COPY package* ./

RUN npm install

COPY . .

RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]