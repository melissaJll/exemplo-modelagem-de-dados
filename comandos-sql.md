# Comandos SQL - Referências 

## Modelagem Física com comandos DLL

### Criar Banco de Dados

CREATE DATABASE vendas CHARACTER SET utf8mb4;
USE DATABASE vendas;

### Criar tabela de fabricantes

```SQL
CREATE TABLE fabricantes(
    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
    nomeFabricante VARCHAR(45) NOT NULL
);
```