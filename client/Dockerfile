FROM node:12.2.0-alpine

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json

RUN npm config set unsafe-perm true

RUN npm install --silent
RUN npm install react-scripts -g --silent

COPY . .

CMD ["npm", "start"]
