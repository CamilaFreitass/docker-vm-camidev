cd camidev.com
docker build -t camidev.com . --no-cache
docker run -d -p 8081:80 camidev.com

cd reg-oco.camidev.com
docker build -t reg-oco.camidev.com . --no-cache
docker run -d -p 8082:8000 reg-oco.camidev.com

cd earthquake.camidev.com
docker build -t earthquake.camidev.com . --no-cache --build-arg CHAVE_GOOGLE_MAPS=<chave>
docker run -d -p 8083:8000 earthquake.camidev.com

Docker compose:

1.Crie uma imagem Docker para cada aplicação

2.docker build -t nome_da_imagem_da_aplicacao .

3. cd docker-compose.yml

4. docker-compose up -d