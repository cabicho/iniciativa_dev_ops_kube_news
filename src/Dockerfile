FROM node:18.11.0
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]
# cd src && docker build -t cabicho/iniciativa_dev_ops_kube_news:v1 .
# docker push cabicho/iniciativa_dev_ops_kube_news:v1
# docker tag cabicho/iniciativa_dev_ops_kube_news:v1 cabicho/iniciativa_dev_ops_kube_news:latest
# docker push cabicho/iniciativa_dev_ops_kube_news:latest