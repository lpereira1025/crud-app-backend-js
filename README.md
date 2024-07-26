<h1>Node API Server</h1>
<h2>Descrição do Projeto</h2>
Este projeto é uma API desenvolvida em Node.js utilizando o framework Express.js e o banco de dados MongoDB. A API permite operações CRUD (Create, Read, Update, Delete) em uma coleção de produtos.

<h2>Tecnologias Utilizadas</h2>
<li>Node.js: Ambiente de execução para JavaScript.</li>
<li>Express.js: Framework web para Node.js, utilizado para criar a estrutura do servidor e gerenciar as rotas.</li>
<li>MongoDB: Banco de dados NoSQL utilizado para armazenar as informações dos produtos.</li>
<li>Mongoose: Biblioteca de modelagem de dados para MongoDB, utilizada para definir os esquemas dos dados e interagir com o banco de dados.</li>

<h2>Funcionalidades</h2>
<li>Listar todos os produtos: Endpoint para obter todos os produtos cadastrados no banco de dados.</li>
<li>Obter um produto específico: Endpoint para obter os detalhes de um produto específico através do seu ID.</li>
<li>Criar um novo produto: Endpoint para adicionar um novo produto ao banco de dados.</li>
<li>Atualizar um produto existente: Endpoint para atualizar as informações de um produto existente através do seu ID.</li>
<li>Excluir um produto: Endpoint para deletar um produto do banco de dados através do seu ID.</li>
  
<h2>Estrutura do Projeto</h2>
<h3>Servidor e Conexão com o Banco de Dados</h3>
O servidor é inicializado através do arquivo principal server.js, onde a conexão com o MongoDB é estabelecida utilizando a biblioteca Mongoose. Caso a conexão seja bem-sucedida, o servidor é iniciado na porta 3000.

<h2>Middleware</h2>
Os middlewares express.json() e express.urlencoded({ extended: false }) são utilizados para processar requisições JSON e dados codificados em URL.

<h2>Rotas</h2>
As rotas para a API de produtos são definidas no arquivo product.route.js e associadas ao caminho /api/products no servidor.

<h2>Controladores</h2>
Os controladores responsáveis pelas operações CRUD são definidos no arquivo product.controller.js. Cada controlador executa uma operação específica no banco de dados e retorna a resposta apropriada.

<h2>Modelos</h2>
O esquema do produto é definido no arquivo product.model.js utilizando Mongoose. O esquema inclui os campos name, quantity, price e image, além de timestamps automáticos.

<h2>Como Executar o Projeto</h2>
<li>Clone este repositório para sua máquina local.</li>
<li>Instale as dependências do projeto utilizando npm install.</li>
<li>Configure a string de conexão do MongoDB no arquivo server.js.</li>
<li>Execute o servidor utilizando npm start.</li>
<li>Acesse a API através do endereço http://localhost:3000/api/products.</li>
  
<h2>Endpoints da API</h2>

<li>GET /api/products: Retorna todos os produtos.</li>
<li>GET /api/products/: Retorna um produto específico pelo ID.</li>
<li>POST /api/products: Cria um novo produto.</li>
<li>PUT /api/products/: Atualiza um produto existente pelo ID.</li>
<li>DELETE /api/products/: Exclui um produto pelo ID.</li>
