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
### Criação do relacionamento entre as tabelas FOREIGN KEY
```SQL
ALTER TABLE produtos
    -- CONSTRAINT = Restrição que indica um relacionamento
    ADD CONSTRAINT fk_produtos_fabricantes FOREIGN KEY (idFabricante)
	REFERENCES fabricantes(id)
;
```

```SQL
```
### Exemplos de alterações estruturais na tabela
#### Renomear tabela

```SQL
ALTER TABLE produtos RENAME TO produtos;
```

#### Novo tipo de dado
```SQL
ALTER TABLE table_name 
    MODIFY COLUMN preco INT NOT NULL;

ALTER TABLE table_name 
    MODIFY COLUMN preco DECIMAL(6,2) NOT NULL;
```

### Renomear colunas

```SQL
ALTER TABLE table_name 
    RENAME COLUMN old_name TO new_column_name VARCHAR(45) NOT NULL;

    ou

ALTER TABLE table_name 
    CHANGE old_name new_name VARCHAR(45) NOT NULL;
```

### Adicionar colunas
```SQL
ALTER TABLE produtos 
    ADD quantidade INT NULL AFTER preco;
```

