FROM ubuntu:latest

EXPOSE 5001

RUN apt update && apt install curl -y

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt install -y nodejs

WORKDIR /app

COPY package* ./

RUN npm install && npm install -g serve

COPY . .

RUN npm run build

CMD ["serve", "-s", "-l", "5001", "build"]