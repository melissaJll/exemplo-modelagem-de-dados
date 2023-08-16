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
```