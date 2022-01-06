## Atividade Fase 4

__*Containerization Strategy*__

## Customização de ContainerFile
Arquivo na raiz do projeto com o nome `ContainerFile`


## Criar blog Openshift

Antes de iniciar a criação do ambiente certifique-se de que o projeto com o nome `fiap` esta criado.

```bash
oc new-project fiap
```

Após a criação do projeto executar o comando abaixo:

```bash
oc apply -k kustomization.yml
```
## Descrição dos entregaveis
`pvc/pvc-database.yml` - Criação do volume persistente para o banco de dados.

`secret/database-secret` - Criação das secrets para usuário/senha e nome da base de dados.

`database/deployment-database.yml` - Criação do banco de dados postgreSQL.

`blog/deployment-blog.yml` - Criação do blog python a partir de um repositório git.

`service/blog-service.yml` - Criação do serviço para iniciar o blog.

`service/database-service.yml` Criação do serviço para iniciar o banco de dados.

`hpa/hpa-blog.yml` - Criação de regra para escalar a blog caso necessário.

`hpa/hpa-database.yml` - Criação de regra para escalar o banco de dados caso necessário.

## License
[MIT](https://choosealicense.com/licenses/mit/)
