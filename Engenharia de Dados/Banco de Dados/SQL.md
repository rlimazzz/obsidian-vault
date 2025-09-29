**SQL** (**_Structured Query Language_**) é a linguagem padrão para Sistemas Gerenciadores de Bancos de Dados Relacionais (SGBDR).

```
CREATE TABLE FUNCIONARIO ( 
	     Pnome VARCHAR(20) NOT NULL,
	     Minicial CHAR(1) NOT NULL,  
	     Unome VARCHAR(20) NOT NULL,  
	     Cpf CHAR(9) NOT NULL,  
	     Datanasc DATE NOT NULL,  
	     Endereco VARCHAR(40) NOT NULL,  
	     Sexo CHAR(1) NOT NULL,  
	     Salario NUMERIC(20,2) NOT NULL,  
	     Cpf_supervisor CHAR(9) NULL,  
	     Dnr INT NOT NULL,  
	     PRIMARY KEY (Cpf),  
	     FOREIGN KEY (Cpf_supervisor) REFERENCES FUNCIONARIO(Cpf)  
	);
```

Brincando com SQL e [[Álgebra Relacional]] , de acordo com o banco de dados usado.

- Exemplo 1:

	SELECT * FROM DEPARTAMENTO 
	WHERE DEPARTAMENTO.Dnumero = 5

- Exemplo 2:

	SELECT Dnome, Dnumero FROM DEPARTAMENTO 
	WHERE DEPARTAMENTO.Dnumero = 5

- Exemplo 3:

	SELECT pnome AS 'Primeiro Nome', unome FROM FUNCIONARIO
	WHERE sexo = 'M'

- Exemplo 4:

	SELECT Pnome AS 'PRIMEIRO NOME', unome, sexo, salario FROM FUNCIONARIO
	WHERE salario BETWEEN 30000 and 40000

- Exemplo 5:

	SELECT Pnome AS 'PRIMEIRO NOME', unome, sexo, salario FROM FUNCIONARIO
	WHERE salario NOT BETWEEN 30000 and 40000

- Exemplo 6:

	SELECT Cpf, Pnome, Unome, Salario FROM FUNCIONARIO
	WHERE Salario NOT IN (40000, 50000, 43000)


