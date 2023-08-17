# Comandos para operações CRUD no banco de dados

## Resumo
- C -> CREATE (inserir dados usando comando `Insert`) 
- R -> READ (ler dados usando o comando  `SELECT`) <!--SELECT coluna_Name FROM table_name; -->
- U -> UPDATE (atualizar dados usando comando `UPDATE`) <!-- UPDATE table_name SET nomeColuna = new_value WHERE id = 1   -->
- D -> DELETE (excluir dados usando comando `DELETE`)
<!-- DELETE from tbl_autores WHERE IdAutor = 19;-->

## INSERT
### 
```sql
INSERT INTO fabricantes(nomeFabricante) VALUES
('Asus'); 
INSERT INTO fabricantes(nomeFabricante) VALUES
('Dell'),('Apple'); 
INSERT INTO fabricantes(nomeFabricante) VALUES
('LG'),('Samsung'),('Brastemp');
INSERT INTO fabricantes(nomeFabricante) VALUES
('Positivo'),('Microsoft');  


INSERT INTO produtos(nomeProduto, preco, descricao, quantidade, idFabricante) VALUES
('Ultrabook', 3500, 'Equipamento de ultima geração cheio de recursoscom processador Intel Core i9', 7, 2);-- Dell = 2

INSERT INTO produtos(nomeProduto, descricao, preco, quantidade, idFabricante) VALUES
('Tablet Android', 'Tablet com a versão 14 do sistema operacional Android', 1500.99, 5, 5);
INSERT INTO produtos(nomeProduto, descricao, preco, quantidade, idFabricante) VALUES
('Geladeira', 'Refrigerador frost-free smart', 5000, 12, 6),
 ('iPhone 18 Pro Max', 'Smartphone Apple', 12666.66, 3, 3),
 ('iPad Mini', 'Tablet Apple', 4999.01, 5, 3);

 INSERT INTO produtos(nomeProduto, descricao, preco, quantidade, idFabricante) VALUES 
 ('Xbox Series S', 'Velocidade e desempenho de última geração', 1997, 5, 8),
 ('Notebook Motion', 'Intel Dual Core 4GB de RAM, 128GB SSD e Tela 14,1 polegadas', 1213.65, 8, 7);


```
## SELECT
<!--SELECT coluna_Name FROM table_name; -->

```sql

SELECT * FROM produtos;
SELECT nomeProduto FROM produtos;
SELECT nomeProduto, preco, quantidade FROM produtos WHERE preco < 5000 ;

SELECT nomeProduto, descricao FROM produtos WHERE idFabricante = 3 ;
```
### Operadores lógicos: AND, OR NOT
#### AND

```sql
SELECT nomeProduto, preco FROM `produtos` WHERE preco >= 2000 AND preco <= 6000;

SELECT nomeProduto, preco FROM `produtos` WHERE preco > 5000 AND preco <= 6000;

```

#### OR
```sql
SELECT nomeProduto, preco FROM `produtos` WHERE preco > 5000 OR preco <= 3000;

SELECT nomeProduto, preco FROM `produtos` WHERE idFabricante = 3 OR idFabricante = 5; 

-- Conteudo Novo Usando FUNÇÃO IN
SELECT nomeProduto, preco FROM `produtos` WHERE idFabricante IN(3,5); 
```


#### NOT

```sql
SELECT nomeProduto, descricao, preco FROM `produtos` WHERE NOT idFabricante = 8;

SELECT nomeProduto, descricao, preco FROM `produtos` WHERE idFabricante != 8;

-- Conteudo Novo Usando FUNÇÃO IN
SELECT nomeProduto, preco FROM `produtos` WHERE idFabricante NOT IN(3,5); 
OU
SELECT nomeProduto, preco FROM `produtos` NOT WHERE idFabricante IN(3,5); 
```

####
<!-- UPDATE table_name SET nomeColuna = new_value WHERE id = 1-->

```sql
UPDATE fabricantes SET nomeFabricantes = 'Asus do Brasil' WHERE id = 1;

UPDATE produtos SET preco = 6549.74 WHERE id = 4;

UPDATE produtos SET preco = 6549.74 WHERE id = 4;

UPDATE produtos SET quantidade = 20 WHERE idFabricante IN(3,5);
```