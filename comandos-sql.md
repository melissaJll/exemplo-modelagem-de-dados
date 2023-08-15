# Comandos

```SQL
CREATE DATABASE catalogo_filmes CHARACTER SET utf8mb4;
USE DATABASE catalogo_filmes;
```
```SQL
DESC filmes;
```

### Criar tabelas

```SQL
CREATE TABLE generos(
    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
    nomeGenero VARCHAR(45) NOT NULL

);

--DROP TABLE filmes;

CREATE TABLE filmes(
    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
    nomeFilme VARCHAR(45) NOT NULL,
    anoLancamento YEAR,
    idGenero INT,
    CONSTRAINT fk_generos_filmes FOREIGN KEY (idGenero)
	REFERENCES generos(id)
);
```
