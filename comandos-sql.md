# Comandos SQL - Referências 

## Modelagem Física com comandos DLL

### Criar Banco de Dados

```SQL
CREATE DATABASE vendas CHARACTER SET utf8mb4;
USE DATABASE vendas;
```

### Criar tabela de fabricantes

```SQL
CREATE TABLE fabricantes(
    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
    nomeFabricante VARCHAR(45) NOT NULL
);
```

### Vizualizar detalhes estruturais da tabela

```SQL
DESC fabricantes;
```

### Criar tabela de produtos

```SQL
CREATE TABLE produtos(
    id INT PRIMARY KEY AUTO_INCREMENT NOT NULL,
    nomeProduto VARCHAR(45) NOT NULL,
    descricao TEXT(500),
    preco DECIMAL(6,2),
    idFabricante INT NOT NULL
);
```


