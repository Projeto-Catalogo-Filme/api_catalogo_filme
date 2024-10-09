# MovieKah - Catálogo de Filmes

Meu primeiro projeto aprimorando habilidades em API e React. Projeto de Catálogo de Filmes, onde você poderá fazer login, e ter acesso a filmes inseridos por você. 

Tive como foco aprimorar habilidades na implementação de um CRUD (Criação, Leitura, Atualização e Exclusão), e fazer as todas as do site, também implementei responsividade.


 # Estrutura das Tabelas
CREATE TABLE tb_filme (
  id_filme			  INT PRIMARY KEY AUTO_INCREMENT,
  nm_filme			  VARCHAR (200) NOT NULL,
  ds_sinopse			VARCHAR (4000) NOT NULL,
  vl_avaliacao 		DECIMAL (15,2) NOT NULL,
  dt_lancamento		DATE NOT NULL,
  bt_disponivel		BOOLEAN NOT NULL,
  img_filme			  VARCHAR (800) NOT NULL,
  id_usuario			INT,
  FOREIGN KEY (id_usuario) REFERENCES tb_usuario (id_usuario)
);

CREATE TABLE tb_usuario (
  id_usuario		INT PRIMARY KEY AUTO_INCREMENT,
  ds_email		  VARCHAR (255) NOT NULL,
  ds_senha 		  VARCHAR (255) NOT NULL
);


 # Variáveis de Ambiente do Backend
 PORTA=5010

 MYSQL_HOST=localhost
 MYSQL_USER=root
 MYSQL_PWD=password
 MYSQL_DB=database
