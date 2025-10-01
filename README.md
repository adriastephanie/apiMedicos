# **Nome do Repositório**


> Este repositório contém o código-fonte e a documentação para o projeto de apis de medicos (CRUD).

## **Pré-requisitos**
# API Voll.med` 

API REST da aplicação Voll.med, desenvolvida com Spring Boot 3.5.6 e Java 17.

## Pré-requisitos

- [Java 17+](https://adoptium.net/)
- [Maven 3.8+](https://maven.apache.org/download.cgi)
- [MySQL](https://dev.mysql.com/downloads/mysql/) (para persistência e migrações Flyway)

## Instalação

Clone o repositório e acesse a pasta do projeto:

```bash
git clone <url-do-seu-repositorio>
cd <nome-da-pasta>
```
## Exemplos de Requisições

### Criar um Médico

```bash
curl --location 'http://localhost:8080/medicos' \
--header 'Content-Type: application/json' \
--data-raw '{
  "nome": "Beatriz Silva",
  "email": "beatriz@teste.com.br",
  "crm": "244433",
  "telefone": "987654321",
  "especialidade": "ORTOPEDIA",
  "endereco": {
    "logradouro": "rua 7",
    "bairro": "Novo",
    "cep": "13073090",
    "cidade": "Campinas",
    "uf": "SP",
    "numero": "123",
    "complemento": "complemento"
  }
}'
```

### Listar Médicos

```bash
curl --location 'http://localhost:8080/medicos'
```

> [!NOTE]
> - O endpoint `/medicos` aceita requisições `POST` para cadastro e `GET` para listagem.
> - Certifique-se de que a aplicação está rodando em `localhost:8080`.
> - Ajuste os dados conforme necessário para seu ambiente.
> - tete

## Estrutura do Projeto

| Pasta/Arquivo                | Descrição                  |
|------------------------------|----------------------------|
| `/src/main/java`             | Código-fonte Java          |
| `/src/main/resources`        | Configurações e migrations |
| `/src/test/java`             | Testes automatizados       |
| `pom.xml`                    | Gerenciamento de dependências |


## Configuração

Crie o arquivo `src/main/resources/application.properties` com as configurações do banco de dados:

```properties
spring.datasource.url=jdbc:mysql://localhost:8080/seu_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=validate
spring.jpa.show-sql=true
spring.flyway.enabled=true
```

> [!TIP]
> Altere os valores conforme seu ambiente local.

## Build e Execução

Para compilar e rodar o projeto localmente:

## Estrutura do Projeto

| Pasta/Arquivo              | Descrição                        |
|----------------------------|----------------------------------|
| `/src/main/java`           | Código-fonte Java                |
| `/src/main/resources`      | Configurações e migrations       |
| `/src/test/java`           | Testes automatizados             |
| `pom.xml`                  | Gerenciamento de dependências    |

## Principais Dependências

- spring-boot-starter-web
- spring-boot-starter-data-jpa
- spring-boot-starter-validation
- spring-boot-devtools
- spring-boot-starter-test
- flyway-core, flyway-mysql
- mysql-connector-j
- lombok

## Contribuição

1. Fork este repositório
2. Crie uma branch: `git checkout -b minha-feature`
3. Commit suas alterações: `git commit -m 'feat: minha nova feature'`
4. Push para o branch: `git push origin minha-feature`
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a licença MIT.