# Minhas Notas do Curso

### Aulas 2 e 3
*  Definir o timezone do banco de dados como UTC é considerado boa prática.

**Flyway** - ferramenta para versionamento de scripts de banco de dados (uso em produção)

*  Nome dos Arquivos do flyway devem começar com a letra V, seguido de algum número (ex.: V001__cria-tabela-cliente.sql).
*  Para abrir o arquivo no STS, clica com botão direito -> Open With -> Text Editor.
*  Se houver problema, para o caso de ter executado um script do flyway sem querer, precisa excluir a linha na tabela do flyway referente ao que você quis fazer, só aí deve tentar novamente.

**Jakarta EE** - especificação guarda-chuva
**Jakarta Persistence** - projeto conhecido como JPA, especificação de API de mapeamento objeto-relacional.
**Hibernate** - implementação da especificação Jakarta Persistence.
*GenerationType.IDENTITY* - Usa forma nativa do banco de dados para incrementar a chave primária.
**Query Methods** - recurso do Spring Data JPA que permite que você faça consultas de pesquisa, ex.: findByNome(String nome), onde a propriedade `nome` existe na entidade Cliente, e não é necessário implementar query, o Spring Data JPA já implementa pra gente. Se o método for assim `findByNomeContaining` com a palavra *Containing*, o Spring Data JPA entende que deve fazer uma query de pesquisa com a cláusula LIKE.
**@ControllerAdvice** - componente do Spring que trata as exception de todos os controllers.
**OffsetDateTime** - padrão ISO8601 - OffsetDateTime é como o LocalDateTime, porém com offset (fuso horário)
** Representation Model** - usando a mesma classe do model (entidade) pra representar a api. O ideal é ter uma classe pra cada camada para evitar problemas, ou seja, uma classe DTO, para transporte de dados.
**ModelMapper** - ajuda a resolver problemas de boilerplate, ou seja, classes model que, por exemplo, tem que ficar preenchendo com getters e setters, para criação de DTOs.
**Idempotente** - PUT é idempotente pois não gera efeitos colaterais quando várias requisições são executadas num mesmo recurso. POST não é idempotente pois cada requisição gera um efeito colateral (cadastra novo registro mesmo sendo as mesmas informações).


# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.2.6.RELEASE/maven-plugin/)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.2.6.RELEASE/reference/htmlsingle/#boot-features-developing-web-applications)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)