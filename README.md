# OpenLib: biblioteca livre

> Modelagem e camada de persistência de um acervo digital universitário: modelo ER, esquema SQL com triggers e procedures e DAOs em Java/JDBC.

![status](https://img.shields.io/badge/status-concluído-success) ![java](https://img.shields.io/badge/Java-8-blue) ![jdbc](https://img.shields.io/badge/JDBC-DAO-lightgrey) ![mysql](https://img.shields.io/badge/MySQL-5-blue)

## Sobre
Projeto da disciplina de Banco de Dados (UFC, 2016). O OpenLib permite que alunos e professores cadastrem materiais digitais (título, ano, editora, autores, área, capa e link) e organizem grupos de acesso por turma. O trabalho cobre o levantamento de requisitos, o modelo entidade-relacionamento, o esquema relacional, consultas complexas, triggers e procedures, e uma camada DAO em Java.

## Estrutura de pastas
```text
MER_Biblioteca.brM, Modelo Relacional.architect   modelos (brModelo e SQL Power Architect)
esquema_openlib.sql                               criação das tabelas
inserts_openlib.sql                               dados de exemplo
power_queries.sql                                 consultas com junções, agregações e subconsultas
triggers_procedures.sql                           regras de integridade e rotinas
src/entity/                                       Livro, Autor, Editora, Area, Usuario, Professor, Grupo e relações N:N
src/dao/interfaces/, src/dao/                     contratos e implementações JDBC (PreparedStatement)
src/factory/ConnectionFactory.java                conexão MySQL
src/main/Main.java                                demonstração
```

## Como executar
```bash
mysql -u root -p < esquema_openlib.sql && mysql -u root -p openlib < inserts_openlib.sql
javac -d bin $(find src -name "*.java") && java -cp "bin:mysql-connector.jar" main.Main
```

## Status
Concluído. Trabalho acadêmico; não recebe manutenção.

## Autor
Ronildo Silva · ronildo.comp@gmail.com
