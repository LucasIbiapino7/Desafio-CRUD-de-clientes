# CRUD de clientes

# Sobre o projeto

Apresenta as cinco operações básicas de um CRUD para recursos, com as principais exceções tratadas com retorno customizado.

## Modelo conceitual
![Modelo Conceitual](https://github.com/LucasIbiapino7/assets/blob/main/imgs/CRUD-clientes.png)

# Tecnologias utilizadas
## Back end
- Java
- Spring Boot
- JPA / Hibernate
- Maven
- Postman
# Competências
- Desenvolvimento em Camadas
- Validação e Tratamento de exceções com respostas customizadas
# Features
- Busca paginada de recursos
- Busca de recurso por id
- Inserir novo recurso
- Atualizar recurso
- Deletar recurso
- Validação para: "name" não pode ser vazio e "birthDate" não pode ser uma data do Futuro.
- Exemplo de resposta quando esses campos não são validados:
```json
{
    "timestamp": "2024-01-30T16:29:34.331772900Z",
    "status": 422,
    "error": "dados inválidos",
    "path": "/clients",
    "errors": [
        {
            "fieldName": "birthDate",
            "message": "Data precisa ser do passado"
        },
        {
            "fieldName": "name",
            "message": "Campo requerido"
        }
    ]
}
```
- Exemplo de resposta quando o Id não é encontrado:
```json
{
    "timestamp": "2024-01-30T16:31:02.148909700Z",
    "status": 404,
    "error": "Recurso Não encontrado",
    "path": "/clients/100"
}
```
# Como executar o projeto

## Back end
Pré-requisitos: Java 11

```bash
# clonar repositório
git@github.com:LucasIbiapino7/Desafio-CRUD-de-clientes.git
```
# Autor

Lucas Ibiapino Do Nascimento Duarte


