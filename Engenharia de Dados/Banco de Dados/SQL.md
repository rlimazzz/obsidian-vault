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

**Quais são os departamentos de número 5?**
	SELECT * FROM DEPARTAMENTO 
	WHERE DEPARTAMENTO.Dnumero = 5

- Exemplo 2:

**Quais são os nomes e números dos departamentos com o número 5?**
	SELECT Dnome, Dnumero FROM DEPARTAMENTO 
	WHERE DEPARTAMENTO.Dnumero = 5

- Exemplo 3:

**Quais são os primeiros nomes e sobrenomes de funcionários do sexo masculino?**
	SELECT pnome AS 'Primeiro Nome', unome FROM FUNCIONARIO
	WHERE sexo = 'M'

- Exemplo 4:

**Qual o primeiro nome, sobrenome, sexo e salario dos funcionários que tem o salário entre 30000 e 40000?**
	SELECT Pnome AS 'PRIMEIRO NOME', unome, sexo, salario FROM FUNCIONARIO
	WHERE salario BETWEEN 30000 and 40000

- Exemplo 5:

**Qual o primeiro nome, sobrenome, sexo e salario dos funcionários que não tem salário entre 30000 e 40000?**
	SELECT Pnome AS 'PRIMEIRO NOME', unome, sexo, salario FROM FUNCIONARIO
	WHERE salario NOT BETWEEN 30000 and 40000

- Exemplo 6:

**Qual o cpf, primeiro nome e sobrenome dos funcionários que não tem o salário igual a 40000, 5000 e 43000?**
	SELECT Cpf, Pnome, Unome, Salario FROM FUNCIONARIO
	WHERE Salario NOT IN (40000, 50000, 43000)


