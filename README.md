# Rails Cheat Sheet!

## Vagrant
    vagrant Init: Inicializa um novo arquivo (vagrantfile) com configurações pré definidas.
    vagrant up: Cria e inicia uma máquina virtual 
    vragrant ssh: conecta na máquina virtual pelo bash
    vagrant suspend: Pausa a máquina vitural
    vagrant halt: para a máquina virtual
    vagrant status: informa o status atual da máquina. 

## Rails
    rails: comando que indica para o cmd que você quer usar as funções do framework rails
    rails new NomeProjeto: Cria um novo projeto.
    rails console: Inicia um console para interação com o aplicativo e o banco. 
    rails server -> rails s -b 0.0.0.0: sobre um servidor rails.
    rails routes: Exibe uma lista de todas as rotas disponíveis

## Rails Scaffold
    rails generate scaffold <Model> <campo:tipo> <campo:tipo>: 
        Scafofold: Cria um conjunto de arquivos para criar, ler, atualizar e deletar registros de um modelo (CRUD).
        <Model>:Nome do modelo.
        <campo:tipo>: Quais são os campos e o seus tipos, se for string não é necessário especificar o tipo.
        
## Rails db

    rails db:create: Cria o banco de dados. 
    rails db:drop: Exclui o banco de dados.
    rails db:migrate: Realiza as migrações pendentes atualizando banco de dados conforme as mudanças realizadas.
    rails dbconsole: Comando usado para conectar ao banco de dados e executar comandos para inspecioná-lo.
    rails db:rollback: Reverte a última migração executada.
    rails db:seed: Executa o arquivo db/seeds.rb.
    rails db:setup: Cria o banco de dados, carrega o esquema e executa o arquivo de sementes em uma única operação.
    rails db:schema:load: Carrega o esquema do banco de dados diretamente a partir do arquivo db/schema.rb. Isso é útil         para criar um novo banco de dados a partir do zero com o esquema definido no arquivo de esquema.

    Configuração do banco -> config/database.yml 
    db/seeds.rb -> Arquivo utilizado para popular o banco de dados.

## Rails generate

    O que são geradores? 
        Comandos que automatizam a criação de partes especificas de um aplicativo web.

        Model Generator: Cria um modelo e sua migração associada para definir a estrutura da tabela no banco de dados.

        Controller Generator: Gera um controlador com ações padrão e suas visualizações correspondentes.

        Migration Generator: Cria um arquivo de migração para fazer alterações no esquema do banco de dados.

        Scaffold Generator: Gera um conjunto completo de código para realizar operações CRUD (Create, Read, Update, Delete)         em um modelo, incluindo modelo, migração, 

        rails generate: Comando principal para gerar códigos usando geradores.

        rails generate controller pagina_inicial (rails g controller...): Gera um controlador chamado "PaginaInicial" e             cria a estrutura básica de arquivos associados, incluindo ações padrão (como "index", "new", "create", etc.) e              suas respectivas visualizações.

        rails destroy controller pagina_inicial (rails d controller...):  Estes comandos destroem (ou removem) o                    controlador "PaginaInicial" e os arquivos associados, revertendo as alterações feitas pelo comando rails generate           controller.

        rails generate controller welcome index: Este comando gera um controlador chamado "Welcome" com uma ação chamada            "index". Ele também cria a estrutura básica de arquivos para essa ação.
        

        

        
# rails -T OU rake --tasks: lista todas as tarefas disponíveis.
    



