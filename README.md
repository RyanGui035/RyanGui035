DROP DATABASE livraria;

CREATE SCHEMA IF NOT EXISTS livraria DEFAULT CHARACTER SET utf8;

USE livraria;

CREATE TABLE IF NOT EXISTS Aluno(
id INTEGER NOT NULL AUTO_INCREMENT,
nome VARCHAR (255) NOT NULL,
email VARCHAR (255) NOT NULL,
telefone VARCHAR (14),
altura DECIMAL(3,2),
PRIMARY KEY (id)
)ENGINE=InnoDB;

INSERT INTO Aluno (id, nome, email, telefone, altura)
VALUES 
(NULL, 'João Pimentel', 'jpapim@gmail.com', '(61) 98787-9987', 1.74),
(NULL, 'João da Silva', 'joao.silva@gmail.com', '(61) 98787-0087', 1.74),
(NULL, 'João Paulo', 'joao.paulo@gmail.com', '(61) 98787-9955', 1.94),
(NULL, 'João Brito', 'joao.brito@gmail.com', '(61) 98799-9999', 1.94),
(NULL, 'José Brito', 'jose.brito@gmail.com', '(61) 98787-9987', 1.94);

CREATE TABLE IF NOT EXISTS Professor(
id INTEGER NOT NULL AUTO_INCREMENT,
nome VARCHAR (255) NOT NULL,
email VARCHAR (255) NOT NULL,
telefone VARCHAR (14),
altura DECIMAL(3,2),
PRIMARY KEY (id)
)ENGINE=InnoDB;

INSERT INTO Professor (id, nome, email, telefone, altura)
VALUES 
(NULL, 'Maria da Silval', 'maria.silva@gmail.com', '(61) 98787-9654', 1.54),
(NULL, 'Florisvaldo Pereira', 'florisvaldo@gmail.com', '(61) 98787-8007', 1.70);

SELECT a.nome AS 'Nome do Aluno',
p.nome AS 'Nome do Professor'
FROM Aluno a, Professor p;

SELECT * FROM Aluno;
SELECT * FROM Professor;
SELECT * FROM Aluno, Professor;








