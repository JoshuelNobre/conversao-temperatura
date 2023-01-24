# pegando a imagem do node
FROM node:18.11.0
# definindo meu diretorio de trabalho
WORKDIR /app
# copiando todos os arquivos do package.json e package-locl.json para o meu diretorio corrente (/app)
COPY package*.json ./
# vai fazer o download de todas as dependencias pra dentro da minha imagem
RUN npm install
# copiar todo o projeto pra dentro da minha imagem
# eu copio todos os arquivos somente depois de copiar as dependencias, 
# pois se copiar todos antes, o npm install será executado sempre que tiver qualquer mudança no código do projeto
COPY . .
# expor a porta 8080
EXPOSE 8080
#  comando de inicialização do node
CMD ["node", "server.js"] 