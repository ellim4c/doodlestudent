FROM ubuntu:16.04 AS builder
WORKDIR /app
RUN apt-get update
RUN apt-get install -y npm curl
RUN apt-get upgrade -y && \
    curl -sL https://deb.nodesource.com/setup_16.x | bash - && \
    apt-get install -y nodejs
RUN npm install -g npm@latest
COPY . .
RUN npm install -g @angular/cli@10.1.7
RUN ng version
RUN npm install
RUN ng build

FROM nginx:latest
COPY --from=builder /app/dist/tlcfront/ /usr/share/nginx/html
