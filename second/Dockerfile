FROM node:20

WORKDIR /app

COPY tsconfig.json .

COPY package* .

RUN npm install

COPY ./prisma . 

RUN npx prisma generate

COPY . .

RUN npm run build

EXPOSE 3000

CMD ["node", "dist/index.js"]
