Minha documentação sobre SQL do canal CFBCURSOS

SQL é uma linguagem de manipulação de dados
Se divide em DDL, DQL, DML e DCL

Extensão
.sql

Tipos de dados:
    Texto: tinytext - text - mediumtext - longtext - char - varchar
    Numerico: tinyint - smallint - mediumint - int/integer - bigint - float - double - decimal
    Temporal: date - datetime - timestamp - year - time


Comandos em DDL:

Criar o banco de dados
CREATE DATABASE nome-do-banco;
CREATE SCHEMA nome-do-banco;

Criar a tabela
CREATE TABLE nome-da-tabela (
    nome-da-coluna tipo-da-coluna restrições
);

Deleta o banco de dados
DROP SCHEMA nome-do-banco;

Deleta a tabela
DROP TABLE nome-da-tabela;

Alterar propriedades da coluna de uma tabela
ALTER TABLE nome-da-tabela MODIFY COLUMN nome-da-coluna ALTERAÇÃO

Adicionar coluna a uma tabela existente 
ALTER TABLE nome-da-tabela ADD nome-da-coluna-adicionada

Excluir coluna de uma tabela existente
ALTER TABLE nome-da-tabela DROP COLUMN nome-da-coluna

Criar chave estrangeira
ALTER TABLE tabela-de-origem ADD CONSTRAINT nome-da-restrição FOREIGN KEY (campo-tabela-origem) REFERENCES tabela-destino (campo-tabela-destino);

