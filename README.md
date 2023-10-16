# Rails Cheat Sheet!

## Vagrant
    vagrant Init: Inicializa um novo arquivo (vagrantfile) com configurações pré definidas.
    vagrant up: Cria e inicia uma máquina virtual 
    vragrant ssh: conecta na máquina virtual pelo bash
    vagrant suspend: Pausa a máquina vitural
    vagrant halt: para a máquina virtual
    vagrant status: informa o status atual da máquina. 
    entrar na pasta vagrant (cd.. para voltar e cd 'diretorio' para entrar) (ls para listar)
    vagrant plugin install vagrant-vbguest: instala o plugin vbguest: esse plugin é uma extensão do Vagrant que facilita a instalação e a atualização das Guest Additions no VirtualBox quando você está gerenciando máquinas virtuais (VMs) VirtualBox com o Vagrant. (caso     dê problema na pasta vagrant, reinstalar o plugin (vbguest)).

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

    rails -T OU rake --tasks: lista todas as tarefas disponíveis.

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
        

## ActiveRecord

    O Active Record é a camada de interação com o banco de dados em aplicativos Ruby on Rails. É uma implementação do padrão de projeto Active Record do padrão MVC.
    
    ORM (Mapeamento Objeto-Relacional): O Active Record mapeia tabelas do banco de dados para classes Ruby e linhas de tabela para instâncias de objetos.
    
    Modelos: Modelos são classes Ruby que herdam de ActiveRecord::Base e representam tabelas no banco de dados. 
    
    Relacionamentos: Facilita a definição de relacionamentos entre modelos, como associações um-para-muitos e muitos-para-muitos.    
    
    Migrações: O sistema de migrações permite versionar o esquema do banco de dados de forma controlada.
    
    Validações: Fornece um mecanismo para definir validações nos modelos, garantindo que os dados atendam a critérios específicos. 
    
    Callbacks: Callbacks permitem adicionar lógica personalizada antes ou depois de ações nos modelos.
    
    Query Interface: Oferece métodos para criar consultas SQL programaticamente, simplificando a busca de dados no banco de dados.

## collect e pluck

    são dois métodos que podem ser usados para extrair informações específicas de uma coleção de registros do banco de dados.

    Collect: Traz os dados, permitindo manipula-los e formar um nova array com os dados manipulados.
    Pluck: Traz somente a informação pura, são ser manipulanda, normalmente traz somente da coluna especificada. 

## Help
    
    Métodos prontos que podem ser utilizadas para auxiliar na view.
    Ajuda a manter o DRY (Don’t Repea Yourself) 
    cities_helper.rb

    Helper link_to

        <%= link_to 'Exibir', '/cities'%>
        <%= link_to 'Exibir', city %>
    
        Um método pronto para facilitar a escrita de links usando código rails

    Helper imagem
        <td><img src=”<%= city.image %>” width=”25px”
        height=”25px”></ td>
        <td><%= image_tag city.image , width: 25, height: 25
        %></td>
        <td><%= image_tag city.image , size: “25x25” %></td>

    Helper data
        <%= Date.today %>
        <%= Date.today.strftime("%d/%m/%Y") %>
        <%= br_date(Date.today) %>
        —------------- helper
        module ApplicationHelper
         def br_date(us_date)
         us_data.strftime("%d;%m;%Y")
         end
        end
        


pry --> ativa o bash

exit --> sai do bash

## PROCESSO
    Vragran Up
    Vagrant ssh
    entrar na pasta vagrant (cd.. para voltar e cd 'diretorio' para entrar) (ls para listar)
    rails s -b 0.0.0.0 --> sobe um servidor rails



    



