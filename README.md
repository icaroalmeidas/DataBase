# DataBase Project - MySQL 
Projeto de Banco de Dados

Requisitos de Software

O cliente Tera Comércio de Produtos S.A, solicitou a modelagem de um banco de dados para cadastro dos seus clientes.
A função da Unidados é a análise dos requisitos junto aos usuários para a correta construção do produto. O cliente deseja que inicialmente os scripts sejam construídos para o Banco de Dados MySQL, porém, posteriormente pode haver mudança no ambiente e consequentemente adaptação dos scripts para outros produtos de SGBD.
O cliente não quer nenhuma informação relativa à vendas ou estoque, desejando somente as informações primárias de Clientes.

O nosso cliente solicitou uma tabela para armazenar os livros que são comercializados pela empresa. A solicitação é somente para livros e não há a necessidade de realizar busca em outras tabelas. Hoje há um funcionário de vendas que tem uma tabela do Excel para guardar esses registros, mas as buscas estão ficando complexas. Decidiu-se então criar um banco de dados separado para esse funcionário.
Após a criação da tabela, deveremos entregar algumas queries prontas para que sejam enviadas para o programador. As queries são as seguintes:
1 – Trazer todos os dados.
2 – Trazer o nome do livro e o nome da editora
3 – Trazer o nome do livro e a UF dos livros publicados por autores do sexo masculino.
4 - Trazer o nome do livro e o número de páginas dos livros publicados por autores do sexo feminino.
5 – Trazer os valores dos livros das editoras de São Paulo.
6 – Trazer os dados dos autores do sexo masculino que tiveram livros publicados por São Paulo ou Rio de Janeiro (Questão Desafio).

# OBS: NO PRIMEIRO MOMENTO VAMOS APENAS FAZER ALGUNS TESTES PARA APRENDER ALGUNS COMANDOS E DEPOIS IREMOS MODELAR O BANCO DE DADOS. 

Criando máquina virtual usando o VirtualBox da Oracle

![image](https://github.com/user-attachments/assets/e77f7126-68cc-4b8d-a60d-d9d245fe2192)

Instalando o Windows 11 na máquina virtual 
![image](https://github.com/user-attachments/assets/9e7713d6-bcaa-4cac-bb5f-2188cb1ff15c)

Máquina virtual instalada e com o MySQL instalado e configurado.
![image](https://github.com/user-attachments/assets/7b69160f-fd6a-4bb1-8885-6e2eca0cd186)

Excelente MySQL instalado e condifurado chegou a hora de criarmos nosso banco de dados, tabela e inserir os atributos.

Aqui temos o nosso codigo de criação do database e a tabela com os atributos.

![image](https://github.com/user-attachments/assets/5de9d890-d305-4b27-b01e-1a6c4db66491)

Abaixo já podemos ver que o nosso database está criado e ativo. 

![image](https://github.com/user-attachments/assets/803da9b5-5981-4f58-9f67-2e0aee90668e)

Vamos criar a nossa tabela.
Selecionamos o nosso database e criamos nossa tabela abaixo.

![image](https://github.com/user-attachments/assets/6e927e48-57f1-402a-a607-f9ef84b6e5aa)
![image](https://github.com/user-attachments/assets/5d395890-ae8b-4f0b-bcd8-766df58156a5)

Criando o codigo de inserção no notepadd++
![image](https://github.com/user-attachments/assets/de0860cc-4969-4dd4-9c0c-de42a5e9e8d6)

Inserindo os dados na tabela e exibindo.
![image](https://github.com/user-attachments/assets/cf6dc7de-8aa0-4cb4-a63c-dd7211bbc15f)

Abaixo usando co comando ALTER TABLE para inserirmos uma coluna de LIVRO_ID para ser a chave primária da nossa tabela.
![image](https://github.com/user-attachments/assets/5ba02d38-71f2-4933-a42b-abd2f9df6365)
![image](https://github.com/user-attachments/assets/0863393c-2c38-48d2-a93e-79df282dbf07)

Após a criação da tabela, deveremos entregar algumas queries prontas para que sejam enviadas para o programador. As queries são as seguintes:

1 – Trazer todos os dados.
![image](https://github.com/user-attachments/assets/349c3b3c-d472-4932-9ecd-0432248f3970)

2 – Trazer o nome do livro e o nome da editora
![image](https://github.com/user-attachments/assets/6ff8a8ea-3b63-4eb9-9137-cb134c96d8ec)

3 – Trazer o nome do livro e a UF dos livros publicados por autores do sexo masculino.
![image](https://github.com/user-attachments/assets/5d514f0c-107f-446c-bacd-7bb5ff5e55ef)

4 - Trazer o nome do livro e o número de páginas dos livros publicados por autores do sexo feminino.
![image](https://github.com/user-attachments/assets/52c42505-3cf0-43f7-a1a5-b46f2758c2f9)

5 – Trazer os valores dos livros das editoras de São Paulo.
![image](https://github.com/user-attachments/assets/b0fe9f00-961d-4bcd-9968-9786094cef72)

6 – Trazer os dados dos autores do sexo masculino que tiveram livros publicados por São Paulo ou Rio de Janeiro (Questão Desafio).
![image](https://github.com/user-attachments/assets/dc85ea8c-a1a2-479d-9503-8c2a036552e3)

Vamos trabalhar neste banco de dados. Criamos o banco de dados e a tabela funcionarios e inserimos os dados. 
![image](https://github.com/user-attachments/assets/b243f3d9-c340-4ecb-9e36-602fa21234c7)

Fizemos uma query básica para olharmos a estrutura da nossa tabela e outra para vermos a quantidade de registros. selecy 
![image](https://github.com/user-attachments/assets/157be514-d857-4ebb-9b21-29fae791dafc)

Traga os funcionarios que trabalhem no departamento de filmes OU no departamento de roupas.
![image](https://github.com/user-attachments/assets/e7161512-b7b8-4a94-8bbc-fbf96ac60328)
Como estamos trabalhando com OR e a segunda condicao é opcional colocamos na primeira condicao quem tem mais chances de uma saida verdadeira, pois a segunda condicao nao será checada nesse caso.

Aqui fizemos uma contagem do numero de colaboradores por departamento. 
Na query utilizamos o select para projetar o nome do departamento e a quantidade de colaboradres, utilizamo o alias para nomear a coluna da contagem  e usamos o group by para agrupar a contagem por departamento. 
![image](https://github.com/user-attachments/assets/92d45eb8-856f-4134-aee0-8eea13abd4a9)

O gestor de marketing pediu a lista das funcionarias (AS) = FEMININO que trabalhem no departamento de filmes ou no departamento lar. Ele necessita enviar um email para as colaboradoras desses dois setores. Aqui vamos usar os operadores OR e AND juntos. 
![image](https://github.com/user-attachments/assets/2e6c53a0-5b35-4e93-b302-2f3488fea8a0)
Desta forma podemos transferir este resultado para o gestor exacutar a tarefa desejada. 

Aqui seguem algumas consultas que podemos extrair sobre a coluna salario. 
![image](https://github.com/user-attachments/assets/916f5116-fd0f-4525-bad4-3530f2bfeba9)

Aqui podemos ver a média dos salarios por departamento.
![image](https://github.com/user-attachments/assets/4ef87302-451d-418f-ae3f-7771efbb8034)

Utilizando o comando UPDATE para atualizarmos nossa tabela. Deve ter muito cuidado ao atualizar uma tabela sem o uso da função WHERE que irá indiciar exatamene o item que deve ser atualizado. Ao usar esse comando de forma inadequada vocÊ poderá atualizar uma tabela inteira causando muiotos problemas. 
Podemos ver que o cliente Liliam está com e-mail vazio, após o uso do comando update conseguimos inserir um e-mail para a cliente. 
![image](https://github.com/user-attachments/assets/cdf20c85-6a5b-4623-9e13-fdc6c72703cb)

Utilizando a função DELETE uma das funções mais perigosas a serem usadas, pois, como o nome mesmo é bem claro vocÊ irá deletar itens do seu banco de dados ou itens da sua tabela.
![image](https://github.com/user-attachments/assets/a799087b-1535-4ff6-bb28-8b05f40147af)

AO USAR DELETE OU UPDATE CUIDADO!

## AGORA QUE FIZEMOS VARIOS TESTES E APRENDEMOS ALGUNS COMANDOS VAMOS APRENDER A MODELAGEM DE BANCO DE DADOS. ALGO SUPER IMPORTANTE PARA ESSA CONSTRUÇÃO.

ALGUNS CONCEITOS SÃO NECESSÁRIOS PARA FAZERMOS ESSA MODELAGEM.

### PRIMEIRA FORMA NORMAL
1 - TODO CAMPO VETORIZADO SE TORNARÁ OUTRA TABELA.
EXEMPLOS: [AMARELO, AZUL, VERMELHO, LARANJA] - ESTE É UM VETOR DE CORES
[GELADEIRA, FOGAO, MICROONDAS] - ESTE É UM VETOR DE ELETRO DOMÉSTICOS
[TELEFONE CELULAR, TELEFONE COMERCIAL] - VETOR DE NUMEROS DE TELEFONES
OU SEJA, VETORES SÃO COMPOSTOS DE ITEMS DE UMA MESMA FAMILIA.

2 - TODO CAMPO MULTI VALORADO SE TORNARÁ OUTRA TABELA OU QUANDO O CAMPO FOR DIVISÍVEL.
CAMPOS MULTI VALORADO SÃO VETORES QUE NÃO SÃO DA MESMA FAMILIA.
EXEMPLOS:
ENDEREÇO: RUA - NAIRRO - CIDADE - ESTADO | [RUA ABC - SÃO JOSÉ - IPIRANGA - BA]

3 - TODA TABELA NECESSITA DE PELO MENOS UM CAMPO QUE IDEINTIFIQUE TODO O REGISTRO INTEIRO(LINHA) COMO SENDO UNICO. 
CHAMADO CHAVE PRIMÁRIA/PRIMARY KEY

### MODELAGEM LÓGICA
Na imagem podemos ver as nossas tabelas com suas colunas, as relações e cardinalidade.
![image](https://github.com/user-attachments/assets/07574e4d-f8b2-457f-b10a-c0100e004af9)

A regra para definir quais tabelas irão receber as chaves estrangeiras são:
#### CHAVE ESTRANGEIRA É A CHAVE PRIMARIA DE UMA TABELA QUE VAI ATÉ A OUTRA TABELA PARA FAZER REFERENCIA ENTRE REGISTROS.
Quando o relacionamento é (1,1) a chave estrangeiras irá para a tabela mais fraca, que será definida pela regra do negócio.

![image](https://github.com/user-attachments/assets/95a3ff6c-e574-4e42-9ba7-7c6a6e69b6aa)

No nosso banco de dados a relação entre a tabela cliente e endereço é um para um(1,1), ou seja, haverá apenas um endereço para cada cliente.
Como o nosso objetivo é ter o cadastro do cliente a tabela cliente é a mais forte.
Quando a relação entre as tabelas tiverem a relação de (0,n) a tabela onde a chave estrangeira irá ser colocada é a que tem a relação n.
No nosso exemplo a relação entre a tabela cliente e a tabela telefone é (0,n), ou seja, não é obrigatório o cliente ter telefone, mas caso, ele queira ele pode colocar mais de um telefone. 

Abaixo podemos ver as nossas tabelas criadas seguindo as regras acima.

![image](https://github.com/user-attachments/assets/0a1c3f79-714a-4175-87df-c75615c67765)

Inserindo dados na tabela cliente.
![image](https://github.com/user-attachments/assets/648b9c38-9f5c-4c4e-a535-669523690eb6)

Inserindo dados na tabela endereço.
Podemos ver na imagem em destaque as chaves estrangeiras na tabela endereço batendo com a chave primaria da tabela cliente. A relação é de (1,1) um para um a chave estrangeira não se repete.
![image](https://github.com/user-attachments/assets/8db0c9f7-1f7f-4d81-98ee-7e49dbd444fa)

Inserindo oa dados na tabela telefone.
Como podemos ver abaixo a chave estrangeira ID_CLIENTE se repete. Pois, o relecionamento entra as tabelas cliente e telefone é (0,n), ou seja, não é obrigatório ter telefone mas se tiver o cliente pode fornecer mais de um. O cliente de IDCLIENTE(chave primeria na tabela cliente) numero 5 tem três telefones.
![image](https://github.com/user-attachments/assets/3cc60af3-3db0-4a27-865c-5c76ad55d752)

Entendendo as partes de uma query.
As etapas são Projeção, seleção e junção.
Projeção: tudo que você quer ver na tela. O SELECT é o responsável pela projeção. 
Na query SELECT * FROM CLIENTE;
Estou solicitando que seja projetada toda a tabela cliente.
![image](https://github.com/user-attachments/assets/27f39e21-c03d-4c8d-89cb-91c7f8602ea4)

Seleção: é um filtragem, ou seja, eu estou filtrando as informações.
Na query SELECT * FROM CLIENTE WHERE SEXO = 'F'; Estou filtrando as informações pelo sexo.
![image](https://github.com/user-attachments/assets/22542f8d-b551-4353-b51b-4074b5ab662c)

Ou seja, SELEÇÃO é um subconjunto do meu conjunto total. 

O FROM mostra a origem de onde virá as informações. Ou seja, a origem.

Junção:





