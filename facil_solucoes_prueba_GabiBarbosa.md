*Fácil Soluções Tecnológicas - Teste de TI para estágio de Desenvolvedor de Sistemas Front-end*



**[ Questão 01 - Construa um script PHP que execute a consulta e liste uma relação contendo... ]**

  

`<?php`



`// Realizando a conexão com o banco utilizando PDO com MySQL`

`$variavelConexao = new PDO("mysql: host=######; port=####; dbname=bancoFacil", "login", "senha");`



`// Criando variáveis para armazenar as consultas`

`$nomeBanco = $variavelConexao->query("SELECT nome FROM Tb_banco");`

`$verba = $variavelConexao->query("SELECT verba FROM Tb_convenio");`

`$codigoContrato = $variavelConexao->query("SELECT codigo FROM Tb_contrato");`

`$dataInclusao = $variavelConexao->query("SELECT data_inclusao FROM Tb_contrato");`

`$valor = $variavelConexao->query("SELECT valor FROM Tb_contrato");`

`$prazo = $variavelConexao->query("SELECT prazo FROM Tb_contrato");`



`// Mostrando o resultado das consultas` 

`foreach ($nomeBanco as $row) {`

​	`echo $row['Nome do Banco'] .'</br>';`

`}`

`foreach ($verba as $row) {`

​	`echo $row['Verba do Convênio'] .'</br>';`

`}`

`foreach ($codigoContrato as $row) {`

​	`echo $row['Codigo do Contrato'] .'</br>';`

`}`

`foreach ($dataInclusao as $row) {`

​	`echo $row['Data de Inclusão'] .'</br>';`

`}`

`foreach ($valor as $row) {`

​	`echo $row['Valor'] .'</br>';`

`}`

`foreach ($prazo as $row) {`

​	`echo $row['Prazo'] .'</br>';`

`}`

`?>`



**[ Questão 02 - Construa uma consulta SQL que liste uma relação contendo... ]**



`SELECT banco.nome, convenio.verba, contrato.data_inclusao,` 

`SUM(contrato.valor) AS "Valor Total",`

`MIN(contrato.data_inclusao) AS "Mais antigo",`

`MAX(contrato.data_inclusao) AS "Mais Recente"`

`FROM Tb_banco AS banco, Tb_convenio as AS convenio, Tb_contrato AS contrato`

`GROUP BY banco.nome, convenio.verba`



