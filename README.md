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

Visite o link para ver os testes que fiz para aprender os comandos: https://github.com/icaroalmeidas/Database_Teste

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





