# Raízes do Nordeste - Back-end API

## Descrição do Projeto

API REST desenvolvida em Java com Spring Boot para gerenciamento de pedidos do sistema Raízes do Nordeste.

O projeto foi desenvolvido utilizando arquitetura em camadas, contendo:

* Controllers
* Services
* Repositories
* Entities
* Enums
* Configurações de segurança

---

# Tecnologias Utilizadas

* Java 17
* Spring Boot 3.3.5
* Spring Web
* Spring Data JPA
* Spring Security
* H2 Database
* Swagger / OpenAPI
* Maven

---

# Requisitos

Antes de executar o projeto, é necessário ter instalado:

* Java JDK 17
* Maven
* Eclipse IDE (ou outra IDE Java)
* Postman (para testes da API)

---

# Estrutura do Projeto

```text
src/main/java/com/raizes/raizesdonordeste
│
├── config
├── controller
├── entity
├── enums
├── repository
├── service
└── RaizesdonordesteApplication.java
```

---

# Variáveis de Ambiente

O projeto utiliza banco H2 em memória para ambiente de desenvolvimento.

Exemplo de configuração:

## .env.example

```env
SPRING_DATASOURCE_URL=jdbc:h2:mem:raizesdb
SPRING_DATASOURCE_USERNAME=sa
SPRING_DATASOURCE_PASSWORD=
```

---

# Como Instalar as Dependências

No terminal do projeto execute:

```bash
mvn clean install
```

---

# Como Executar o Projeto

## Pela IDE

1. Abrir o projeto no Eclipse
2. Localizar a classe:

```text
RaizesdonordesteApplication.java
```

3. Executar como:

```text
Run As → Spring Boot App
```

---

## Pelo terminal

```bash
mvn spring-boot:run
```

---

# Banco de Dados

O projeto utiliza banco H2 em memória.

## Acesso ao H2 Console

Após iniciar a aplicação:

```text
http://localhost:8080/h2-console
```

### Configuração:

```text
JDBC URL: jdbc:h2:mem:raizesdb
User Name: sa
Password:
```

---

# Documentação Swagger

Após iniciar a aplicação, acessar:

```text
http://localhost:8080/swagger-ui/index.html
```

---

# Endpoints Principais

## Usuários

```http
POST /usuarios
GET /usuarios
```

## Produtos

```http
POST /produtos
GET /produtos
```

## Pedidos

```http
POST /pedidos
GET /pedidos
GET /pedidos/canal/{canal}
```

## Pagamentos Mock

```http
POST /pagamentos/mock
```

---

# Como Rodar os Testes

Os testes podem ser executados utilizando o Postman.

## Exemplos de testes realizados

### Testes Positivos

* Login com credenciais válidas
* Consulta de produtos
* Criar pedido válido
* Consulta de pedidos por canal
* Atualizar status do pedido
* Pagamento mock aprovado

### Testes Negativos

* Acesso sem token
* Produto inexistente
* Perfil sem permissão
* Canal de pedido inválido
* Pedido sem cliente associado

---

# Segurança

O projeto utiliza Spring Security para autenticação básica.

Usuário e senha gerados automaticamente aparecem no console da aplicação ao iniciar o sistema.

---

# Histórico de Commits Recomendado

## Commit 1

```bash
git commit -m "estrutura inicial do projeto spring boot"
```

## Commit 2

```bash
git commit -m "criação das entidades e repositories"
```

## Commit 3

```bash
git commit -m "implementação dos services e controllers"
```

## Commit 4

```bash
git commit -m "configuração de segurança e swagger"
```

## Commit 5

```bash
git commit -m "implementação dos testes e documentação"
```

---

# Autor

Projeto desenvolvido para fins acadêmicos.
