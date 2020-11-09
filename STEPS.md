## Instalação

    $ npm install serverless -g

    $ serverless create --template aws-nodejs --path <nome_do_projeto>

## Configuração AWS

### Acesse http://console.aws.amazon.com/

<i>É requerido que seja criada uma conta (pode ser de nível gratuito).</i>

> IAM > Usuários > Adicionar usuário

- Digite o nome de usuário (ex: nodeless).
- Selecione a opção **Acesso programático** para que gere uma chave de API e chave de acesso secreta.

> Permissões > Anexar políticas existentes de forma direta

- Selecione a opção **AdministratorAccess**.

> Tags > Revisar > Criar usuário

- Copie o **ID da chave de acesso** e a **Chave de acesso secreta**.

### Configuração local

    $ cd <nome_do_projeto>

    $ serverless config credentials -o --provider aws --key=<ID_chave_acesso> --secret <chave_secreta>

### Deploy

    $ serverless deploy -v

Será criado um Bucket no serviço **Amazon S3**, uma função no **AWS Lambda** e uma Stack no **CloudFormation** (região **us-east-1** se não for especificada).

#### <i>Para remover todos os registros recém criados</i>

    $ serverless remove

## Executar a função

### Formas:

- ### Por rotas HTTP

- ### Por eventos

- ### Por linha de comando

  ```
  $ serverless invoke -f <nome_da_funcao> -l
  ```
