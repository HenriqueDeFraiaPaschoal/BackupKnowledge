SELECT * FROM tabela join

## CREATE
Inicialmente, mas dependendo da ferramenta sendo utilizada, é necessário criar uma database para adicionar as tabelas do projeto.

### Tipos
INT
VARCHAR(n)
TIMESTAMP
BOOLEAN
DECIMAL


CREATE TABLE produtos (
    prod_id INT AUTO_INCREMENT PRIMARY KEY,
    prod_nome VARCHAR(50) NOT NULL,
    prod_qtd_estoque INT NOT NULL DEFAULT 0,
    prod_estoque_min INT NOT NULL DEFAULT 0,
    prod_data_fabricacao TIMESTAMP DEFAULT now(),
    prod_perecivel BOOLEAN,
    prod_valor DECIMAL(10,2),
    marca_id INT,
    CONSTRAINT fk_marcas FOREIGN KEY(marca_id) REFERENCES marcas(marca_id)
);

insert into marcas (marca_id, marca_nome, marca_origem) values (null, 'Faber Castel'	, 'Brasil');
insert into fornecedores values (null, 'Linux','linux@linux.br');

#### VIEW
CREATE VIEW Top10MaisCaros AS SELECT prod_id, prod_nome, prod_valor FROM produtos ORDER BY prod_valor DESC LIMIT 10;

CREATE OR REPLACE VIEW produtos_marcas as
	SELECT
    	prod_nome 'Nome do Produto',
        marca_nome 'Marca',
        prod_valor 'Preço',
        prod_qtd_estoque 'Estoque',
        CASE
        	WHEN prod_perecivel = FALSE THEN 'NÃO'
            WHEN prod_perecivel = TRUE THEN 'SIM'
        END
        'Perecivel'
        FROM
        	produtos LEFT JOIN marcas
            	ON produtos.marca_id = marcas.marca_id
        ORDER BY prod_nome;

CREATE OR REPLACE VIEW produtos_fornecedores as
	SELECT
    	prod_nome,
        forn_nome
        FROM
        	produtos lEFT JOIN produto_fornecedor
            ON produtos.prod_id = produto_fornecedor.prod_id
        ORDER BY prod_nome;


## READ
SELECT * FROM tabela
SELECT prod_id, prod_nome, prod_valor FROM produtos ORDER BY prod_valor DESC LIMIT 10;

SELECT Animais.nome, Especies.alimentacao, Animais.cor FROM
Animais INNER JOIN Especies on
Animais.especie_id = Especies.is WHERE
Especies.alimentacao = 'carnivoro' AND Animais.cor IN ('branco','preto','branca','preta');

WHERE DAY(Animais.data_nasc) < 1;
WHERE YEAR(Animais.data_nasc) < 2023;
WHERE Animais.data_nasc < '2023-01-01';


#### JOIN
SELEC

## UPDATE
UPDATE Pessoas SET idade = 23;
UPDATE Pessoas SET idade = 23 WHERE id = 4;


## DELETE
DELETE Pessoas WHERE idade < 18;

DROP DATABASE Loja;
DROP TABLE Pessoas;

## TABLES
ALTER TABLE Tabela ADD COLUMN nome_campo definição

ALTER TABLE Produtos ADD COLUMN data_validade date;
ALTER TABLE Produtos ADD CONSTRAINT pkProdutos PRIMARY KEY(id);

ALTER TABLE Tabela MODIFY nome_campo Nova_definição

ALTER TABLE Fornecedores MODIFY email VARCHAR(60);
ALTER TABLE Produtos MODIFY DECIMAL(9,2) NOT NULL;
ALTER TABLE Fornecedores DROP COLUMN cnpj;


UPDATE Animais SET Animais.nome = 'Goofy' WHERE Animais.nome = 'Pateta';
UPDATE Animais SET Animais.peso = 10 WHERE Animais.nome = 'Garfield';
UPDATE Animais SET Animais.cor = 'laranja' WHERE especie_id = 1;
ALTER TABLE Animais ADD COLUMN altura INT;
ALTER TABLE Animais ADD COLUMN observacoes VARCHAR(100);
SELECT * FROM Animais WHERE peso > 200;
DELETE * FROM Animais WHERE nome LIKE 'c%';
DELETE Animais FROM Animais WHERE nome LIKE 'c%';

UPDATE Animais SET cor = 'laranja' FROM Animais JOIN Especies ON Animais.id = Especies.id WHERE Especies.nome = 'gato';
ALTER TABLE Animais ADD COLUMN altura DECIMAL(5,2);
ALTER TABLE Animais ADD COLUMN observacao TEXT;
DELETE FROM Animais WHERE peso > 200;
DELETE FROM Animais WHERE nome LIKE 'C%';
ALTER TABLE Animais DROP COLUMN cor;
SELECT * FROM INFORMATION_SCHEMA.COLUMNS;
ALTER TABLE Animais ALTER COLUMN nome VARCHAR(80)
DELETE Animais FROM Animais INNER JOIN Especies ON Animais.id = Especies.id WHERE Especies.nome IN ('gato', 'cachorro');
ALTER TABLE Animais DROP COLUMN data_nasc;
DROP TABLE Especies;
DROP TABLE Animais;

FUNÇÃO DE AGRAGAÇÃO
SELECT MAX (preço) FROM produtos;
SELECT COUNT (id) FROM clientes;
SELECT SUM (peso) FROM pacientes;

GROUP BY
SELECT cor FROM Animais GROUP BY cor;
parecido com o order by mas ele consolida valores iguais, 

SELECT cor, COUNT(ID) FROM Animais GROUP BY cor;
SELECT cor, AVG(peso) FROM Animais GROUP BY cor;
SELECT cor, AVG(peso) FROM Animais GROUP BY cor HAVING AVG(peso) > 15;
SELECT cor, sum(peso) FROM Animais GROUP BY cor;

SELECT MIN(peso) FROM Animais;
SELECT MIN(peso) AS Menor_Peso FROM Animais;
SELECT MAX(peso) FROM Animais;
SELECT TOP number|percent column_name(s) FROM table_name WHERE condition;
SELECT TOP 5 * FROM Animais;
SELECT TOP 50 PERCENT * FROM Animais;
