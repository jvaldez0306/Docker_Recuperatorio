FROM node:16 as build-step
RUN npm install -g http-server
RUN mkdir -p /app
WORKDIR /app
COPY package.json /app
RUN npm install
COPY . .
RUN npm run build --prod

EXPOSE 8080
CMD ["http-server", "public"]