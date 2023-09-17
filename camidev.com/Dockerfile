FROM nginx:latest

RUN apt-get update && apt-get install -y git

RUN rm -rf /usr/share/nginx/html/*

RUN git clone https://github.com/CamilaFreitass/meu_site.git /usr/share/nginx/html

CMD ["echo", "Contêiner concluído!"]

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]