### **Configuração do Spring Initializr**

Acesse: https://start.spring.io

##### Projeto
- Project: Maven Project
- Language: Java
- Spring Boot: 3.3.x (ou versão estável mais recente)
- Packaging: Jar
- Java: 17 ou 21

##### Metadata
- Group: com.cleancar
- Artifact: lavacar
- Name: LavaCar
- Description: Sistema de gerenciamento para Lava Jato CleanCar Express
- Package name: com.cleancar.lavacar
- Packaging: Jar

##### Dependências
Selecione as seguintes:

### Backend / Core

- Spring Web — para criar API REST.

- Spring Boot DevTools — para recarregamento automático durante o desenvolvimento.

- Spring Data JPA — para acesso ao banco de dados com ORM.

- Validation — para validações de campos (ex: @NotNull, @Email).

- Spring Security (opcional, se quiser controle de acesso por função).

### Banco de Dados

**SQL Server Driver** — já que o SGBD do projeto é o Microsoft SQL Server.

### Utilitários

**Lombok** — reduz código repetitivo (getters, setters, construtores).

## Banco de Dados **(application.properties)**

Depois de gerar o projeto, configure:

```conf
spring.datasource.url=jdbc:sqlserver://localhost:1433;databaseName=cleancar;encrypt=false
spring.datasource.username=sa
spring.datasource.password=suasenha
spring.datasource.driver-class-name=com.microsoft.sqlserver.jdbc.SQLServerDriver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.SQLServerDialect
```

Estrutura recomendada de pacotes

```txt
src/main/java/com/cleancar/lavacar
│
├── controller      # Endpoints REST
├── model           # Entidades JPA
├── repository      # Interfaces do Spring Data JPA
├── service         # Regras de negócio
└── dto             # Objetos de transferência de dados
```
### Entidades iniciais

```
Cliente
Veiculo
Funcionario
Servico
Atendimento
```

### Relacionamentos:
```
Cliente 1:N Veículo
Atendimento N:N Serviço
Funcionário 1:N Atendimento
```