# API REST na Nuvem (Santander Bootcamp)

Este projeto tem como objetivo atender ao requisito do Bootcamp FullStack Java & Angular oferecido em conjunto pela DIO e Santander Universidades.

## Tecnologias e Dependencias aplicadas:
- Java
- Gradle
- H2 Database
- PostgreSQL
- SpringBoot Web
- SpringBoot JPA

## Diagrama de Classes

```mermaid
classDiagram
  class Person {
    - name: String
    - account: Account
    - features: Feature[]
    - card: Card
    - news: News[]
  }

  class Account {
    - number: String
    - cc: String
    - dig: String
    - accountBalance: Double
    - accountLimit: Double
  }

  class Feature {
    - icon: String
    - description: String
  }

  class Card {
    - number: String[]
    - limit: Double
  }

  class News {
    - icon: String
    - description: String
  }

  Person "1" *--> "1" Account
  Person "1" *--> "1..n" Feature
  Person "1" *--> "1" Card
  Person "1" *-->  "1..n" News

```