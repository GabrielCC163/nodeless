# Serverless com NodeJS e AWS Lambda

## **Função para otimizar imagens**

<i>[Tutorial da RocketSeat no YouTube](https://www.youtube.com/watch?v=jiP45rEOEbA)</i>

### Instalação

    $ git clone git@github.com:GabrielCC163/nodeless.git
    $ cd nodeless && npm i

### Deploy

Caso for criar um novo bucket, certifique-se de alterar as três ocorrências de "rocketnodeserverlessgrodrigues" no arquivo serverless.yml, para um nome único de bucket.

    $ npm install serverless -g
    $ serverless deploy -v

### Uso da função optimize

- No console da AWS, acesse ao bucket rocketnodeserverlessgrodrigues, e faça o upload de uma imagem.

- Visualize a execução automática da função acessando o serviço **CloudWatch** e então clique em Logs > Grupos de logs > /aws/lambda/nodeless-dev-optimize > Log stream

- Será criada uma pasta 'compressed' com a imagem otimizada dentro.
