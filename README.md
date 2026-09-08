# Lab 1 — Configuração do Ambiente

Template de partida para o **Lab 1** de Distributed Systems 2026/27.

Ao contrário dos templates seguintes, este está deliberadamente quase vazio. O Lab 1 é onde geras o teu primeiro projeto Spring Boot tu próprio, a partir do [start.spring.io](https://start.spring.io), e aprendes mais fazendo isso do que recebendo um já pronto.

## A usar este template

Carrega em **Use this template → Create a new repository**. Dá-lhe o nome `lab-01-environment-setup-aXXXXXXXX`, por exemplo `lab-01-environment-setup-a20250123`. Em minúsculas, sem espaços, número de aluno com o `a` à frente — é a regra em toda a cadeira, e associamos repositórios a alunos pelo número.

## O que vai aqui dentro

Gera o projeto com as definições em
[O teu primeiro projeto Spring Boot](https://github.com/DistributedSystems-Lusofona27/course-docs/blob/main/labs/lab-01-environment-setup/first-spring-boot-project.md)
e faz commit dele para este repositório:

- Group `pt.ulusofona.cd`, artifact `hello-service`, package `pt.ulusofona.cd.hello`
- Java 25, Spring Boot 4.1.0, Maven
- Dependência: Spring Web

A aplicação corre na porta 8080 e responde em `/hello`.

## Antes de entregares

- [ ] `./mvnw clean package` tem sucesso a partir de um clone novo
- [ ] `./mvnw spring-boot:run` arranca e `/hello` responde
- [ ] A raiz do package é `pt.ulusofona.cd.hello` — não `com.example.*`
- [ ] Mais do que um commit, com mensagens que dizem o que mudou
- [ ] `target/` não está committed

Os detalhes completos, incluindo como é avaliado, estão na página de
[Entrega](https://github.com/DistributedSystems-Lusofona27/course-docs/blob/main/labs/lab-01-environment-setup/delivery.md).
