
cd camidev.com
docker build -t camidev.com .
docker run -d -p 8083:80 camidev.com


# docker network create web
# docker-compose up -d
