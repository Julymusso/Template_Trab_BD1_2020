# TRABALHO 01:  Barbearia Gourmet Style Hair
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
primeiro_componente_do_grupo:Carlos Henrique Costa Matos

segundo_componente_do_grupo:Juliana Ricato Musso

segundo_componente_do_grupo:Rodolfo Gomes


### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados Barbearia Gourmet Style Hair
<br>
> A motivação para desenvolver esse projeto, é em virtude das dificuldades do administrador da barbearia. Ele relatou que estava ficando cada vez mais difícil manter o
controle dos dados, pois algumas informações ele não tinha onde armazenar, e ou, não sabia como registrar. Os dados eram registrados em agendas, logo ele guardava muitas
informações desnecessárias. Além disso, de forma desorganizada em relação aos clientes.
De serviços e estoque, o administradorr não possuía controle, era tudo feito a partir do
que elr conseguia observar. O controle era feito da seguinte forma: Com relação aos serviços ele não sabia se
algum funcionário estava realizando poucos, ou nenhum, e não tinha controle sobre os produtos usados pelo mesmo. 
Já as informações dos funcionários, não existia nenhum vínculo empregatício, ou seja, apenas informações de que ele se lembrava: nome,
aniversário, salário, endereços, etc.
Portanto solicitei ao administrador que o seu negócio fosse o objeto de estudo, para algumas disciplinas da faculdade. E neste arquivo estão contidas as informações
pertinentes ao Banco de Dados do projeto.<br>

### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente  real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> Para melhorar o gerenciamento da barbearia Style Hair, Carlos Rodolfo Musso pretende contratar um software para auxiliá-lo. 
Atualmente a barbearia conta com 1 atendente e 6 funcionários divididos entre as funções de barbeiro/cabeleireiro, podólogo e depilador. 
O agendamento funciona da seguinte forma: os clientes ligam para a barbearia ou vão até lá pessoalmente. O atendente consulta se já existe um cadastro desse cliente, em caso positivo, consulta também a agenda do profissional que irá realizar o serviço e confirma o agendamento  informando ao cliente a data, hora, tipo do serviço e nome do prestador.
Caso o cliente não possua cadastro, o atendente solicita informações essenciais como nome completo, cpf, endereço, telefone para contato e email.
A barbearia não atende cliente sem agendamento.
Ao chegar à barbearia na data e hora marcada, o cliente procura o atendente que abre uma ordem de serviço e realiza uma breve entrevista para acrescentar informações adicionais ao cadastro.
O atendente adiciona informações sobre possíveis alergias a determinados produtos ou sobre problemas de saúde que possam ser relevantes para a prestação do serviço. Esses dados deverão ser atualizados a cada atendimento realizado a esse cliente.
O cliente é encaminhado para cada profissional realizar o serviço solicitado. Ao final de todos os serviços as OS são fechadas e o cliente retorna ao atendente para realizar o pagamento.
 

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

![Alt text](https://github.com/Julymusso/Trab_BD1_2021_Barbearia_Gourmet/blob/master/images/Prototipo.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para a Barbearia Gourmet](https://github.com/Julymusso/Trab_BD1_2021_Barbearia_Gourmet/blob/master/arquivos/Prototipo_Barbearia_Gourmet.pdf)

#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    *Relatório que exibe o histórico de serviço do cliente. O relatório deve conter o nome e cpf do cliente. Em cada linha, o nome do funcionário que atendeu, o tipo de serviço solicitado e os  respectivos valores, data e hora. 
    *Faturamento por período. O fatura por período deve exibir todos os serviços prestados pela barbearia dentro do período solicitado, suas respectivas datas e valores e a soma total.
    *Produtividade do funcionário. O relatório deve conter o nome e cpf do funcionário e o período solicitado. Em cada linha, os tipos de serviços realizados com data, hora e valor. Por fim, o valor total capitalizado no período.
    *Agendamentos do dia. O relatório deve conter quais os serviços agendados para o dia, a data e hora e o nome do funcionário responsável, o nome e telefone do cliente.
    *Ordem de Serviço. A OS deve conter todos os dados do cliente (exceto endereço), os tipos de serviço com suas respectivas horas, datas e valores. Por fim o valor total da OS.

   
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/Julymusso/Trab_BD1_2021_Barbearia_Gourmet/blob/master/images/Prototipo.pngraw=true "Tabela - Empresa Devcom")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
    Pessoa,Funcionario,Serviço, Ordem de serviço      
    C) Principais fluxos de informação/entidades do sistema (mínimo 3).
    Pessoa -> solicita -> serviço
    Funcionario -> executa -> ordem de serviço
    Ordem de serviço -> requisita -> serviço
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/Julymusso/Trab_BD1_2021_Barbearia_Gourmet/blob/master/images/Trabalho_1_Conceitual_v3.png?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
------------------------------
    endereco: Tabela que armazena as informações relativas ao cliente<br>
    
    tipologradouro: campo que armazena o tipo de logradouro que a pessoa mora.<br>
    logradouro: campo que armazena o logradouro que a pessoa mora.<br>
    numero: campo que armazena o numero da abitação que a pessoa mora
    bairro: campo que armazena o bairro que a pessoa mora
    cidade: campo que armazena a cidade em que a pessoa mora
    estado: campo que armazena o estado em que a pessoa mora
    cep: campo que armazena o cep da casa da pessoa
    id_endereco: campo que armazena o id do endereço


    executa: Tabela que armazena as chaves que ligam as tabelas ordem_servico e pessoa
    
    fk_funcionario_fk_pessoa_id_pessoa: campo que armazena a chave estrangeira
    fk_ordem_servico_id_os: campo que armazena a chave estrangeira
    
    
    funcionario: Tabela que armazena as informações relativas ao funcionario<br>
    
    cargo: cargo do funcionario na barbearia
    fk_pessoa_id_pessoa: chave estrangeira de funcionario
    
    
    ordem_servico Tabela que armazena as informações relativas as ordens de servico do salão<br>
    
    id_os: codigo id da ordem de serviço
    data: data que o serviço sera feito
    hora: hora em que o serviço sera feito
    status: agendado(a)/executado(a)/não executado(a)
    fk_pessoa_id_pessoa: chave estrangeira de ordem_servico
    
    
    pessoa: Tabela que armazena as informações relativa as pessoas
    
    id_pessoa: numero de identificação de cada pessoa no salão
    cpf: numero do CPF da pessoa cadastrada
    nome: nome da pessoa cadastrada
    sobrenome: sobrenome da pessoa cadastrada
    telefone: telefone da pessoa cadastrada
    email: email da pessoa cadastrada
    fk_endereco_id_endereco: chave estrangeira de pessoa
    
    
    requisita Tabaela que faz a junção entre servico e a orden de servico
    
    fk_servico_id_servico chave estrangeira
    fk_ordem_servico_id_os chave estrangeira
    
    
    servico Trabela com as informações dos serviços que serão realizados
    
    tipo_servico: tipo do corte de cabelo que sera feito
    id_servico: numero de identificação desse serviço
    valor: valor do serviço
------------------------------
### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)
![Alt text](https://github.com/Julymusso/Trab_BD1_2021_Barbearia_Gourmet/blob/master/images/Trabalho_1_Logico_v3.png?raw=true "Modelo Conceitual")
 
### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    
    ordem_servico_2021_12_17 = pd.read_sql_query("select * from ordem_servico where data = '2021-12-17'", comn)
    
    servico_valor = pd.read_sql_query("select * from servico where valor >= 20 and valor < 50", comn)
    
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado

    select pessoa.nome, pessoa.cpf, funcionario.cargo, endereco.logradouro,
    ordem_servico.data, funcionario_ordem_servico.fk_funcionario_fk_pessoa_id_pessoa,
    ordem_servico_servico.fk_servico_id_servico, servico.valor
    from pessoa 
    join funcionario 
    on (pessoa.id_pessoa = funcionario.fk_pessoa_id_pessoa)
    join endereco
    on (endereco.id_endereco = pessoa.fk_endereco_id_endereco)
    join ordem_servico 
    on(ordem_servico.fk_pessoa_id_pessoa = pessoa.fk_endereco_id_endereco)
    join funcionario_ordem_servico
    on(funcionario_ordem_servico.fk_funcionario_fk_pessoa_id_pessoa = ordem_servico.fk_pessoa_id_pessoa)
    join ordem_servico_servico
    on(funcionario_ordem_servico.fk_funcionario_fk_pessoa_id_pessoa = ordem_servico_servico.fk_servico_id_servico)
    join servico
    on(servico.id_servico = ordem_servico_servico.fk_servico_id_servico)
    group by pessoa.nome, pessoa.cpf, funcionario.cargo, endereco.logradouro, ordem_servico.data, funcionario_ordem_servico.fk_funcionario_fk_pessoa_id_pessoa,
    ordem_servico_servico.fk_servico_id_servico, servico.valor
    order by pessoa.nome asc

    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

    -- 1 pessoa e seu endereco
    select pessoa.nome, pessoa.cpf, endereco.logradouro, endereco.bairro, endereco.cidade
    from pessoa 
    join funcionario 
    on (pessoa.id_pessoa = funcionario.fk_pessoa_id_pessoa)
    join endereco
    on(pessoa.id_pessoa = endereco.id_endereco)
    group by pessoa.nome, pessoa.cpf, endereco.logradouro, endereco.bairro, endereco.cidade
    order by pessoa.nome asc

    -- 2 quem são funcionarios
    select pessoa.nome, pessoa.cpf, funcionario.fk_pessoa_id_pessoa
    from pessoa as pessoa
    join funcionario as funcionario
    on (pessoa.id_pessoa = funcionario.fk_pessoa_id_pessoa)
    group by pessoa.nome, pessoa.cpf, funcionario.fk_pessoa_id_pessoa
    order by pessoa.nome asc
    
    -- 3 funcionario
    select pessoa.nome, funcionario.cargo, servico.id_servico
    from pessoa as pessoa
    join funcionario
    on(funcionario.fk_pessoa_id_pessoa = pessoa.id_pessoa)
    join servico
    on(funcionario.fk_pessoa_id_pessoa = servico.id_servico)
    group by pessoa.nome, funcionario.cargo, servico.id_servico
    order by servico.id_servico asc

    -- 4 atividades que faz
    select pessoa.nome, funcionario.cargo, servico.tipo_servico
    from pessoa as pessoa
    join funcionario
    on(funcionario.fk_pessoa_id_pessoa = pessoa.id_pessoa)
    join servico
    on(funcionario.fk_pessoa_id_pessoa = servico.id_servico)
    group by pessoa.nome, funcionario.cargo, servico.tipo_servico
    order by funcionario.cargo asc

    -- 5 valores dos servicos
    select servico.tipo_servico, servico.valor
    from ordem_servico as ordem_servico
    join servico
    on(servico.id_servico = ordem_servico.fk_pessoa_id_pessoa)
    group by servico.tipo_servico, servico.valor
    order by servico.tipo_servico asc

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção
    
     valores_sevico = pd.read_sql_query(""" select ordem_servico.data, servico.valor,count(ordem_servico.data) 
     as ordem_de_servicos from ordem_servico join servico as servico 
     on(ordem_servico.id_os = servico.id_servico)
     where ordem_servico.data = '2021-12-04' group by ordem_servico.data, servico.valor """, comn)
     
     cliente_bairro = pd.read_sql_query(""" select pessoa.nome, endereco.bairro, count(endereco.bairro) 
     from pessoa as pessoa join ordem_servico as ordem_servico 
     on(pessoa.id_pessoa = ordem_servico.id_os) join endereco 
     on (pessoa.fk_endereco_id_endereco = endereco.id_endereco) 
     where endereco.cidade = 'Vitoria'
     group by pessoa.nome, endereco.bairro""", comn)
     
     cliente_bairro_VV = pd.read_sql_query(""" select pessoa.nome, endereco.bairro, count(endereco.bairro) 
     from pessoa as pessoa join ordem_servico as ordem_servico on(pessoa.id_pessoa = ordem_servico.id_os) 
     join endereco on (pessoa.fk_endereco_id_endereco = endereco.id_endereco) 
     where endereco.cidade = 'Vila Velha'
     group by pessoa.nome, endereco.bairro""", comn)

     cliente_bairro_Serra = pd.read_sql_query(""" select pessoa.nome, endereco.bairro, count(endereco.bairro) 
     from pessoa as pessoa join ordem_servico as ordem_servico
     on(pessoa.id_pessoa = ordem_servico.id_os) join endereco 
     on (pessoa.fk_endereco_id_endereco = endereco.id_endereco) 
     where endereco.cidade = 'Serra'
     group by pessoa.nome, endereco.bairro""", comn)
     
     valores_sevico_2 = pd.read_sql_query(""" select ordem_servico.data, servico.valor, count(ordem_servico.data) as ordem_de_servicos 
     from ordem_servico join servico as servico on(ordem_servico.id_os = servico.id_servico)
     where ordem_servico.data = '2021-12-04' and valor >= 39.0 and valor <= 44.0 group by ordem_servico.data, servico.valor """, comn)

     ordem_servico_valores = pd.read_sql_query("""select ordem_servico.data, servico.valor, count(ordem_servico.data) 
     as ordem_de_servicos from ordem_servico join servico as servico 
     on(ordem_servico.id_os = servico.id_servico)
     where ordem_servico.data >= '2021-12-04' group by ordem_servico.data, servico.valor """, comn)

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

    --1 left pessoa e cargo
    select pessoa.nome, funcionario.cargo as cargo
    from pessoa as pessoa
    left join funcionario on (funcionario.fk_pessoa_id_pessoa = pessoa.id_pessoa)
    where funcionario.cargo is not null
    order by pessoa

    -- 2 right -cargos
    select funcionario.cargo as cargo
    from funcionario
    right join ordem_servico 
    on (ordem_servico.id_os = funcionario.fk_pessoa_id_pessoa)
    where funcionario.cargo is not null
    order by ordem_servico.id_os

    --3 full join pessoa e seu endereco
    select pessoa.nome, endereco.logradouro, endereco.bairro, endereco.cidade as cidade
    from endereco
    full join pessoa
    on (pessoa.fk_endereco_id_endereco = endereco.id_endereco)

    --4 full join pessoa e onde reside
    select pessoa.nome, endereco.logradouro, endereco.bairro, endereco.cidade as cidade 
    from endereco full join pessoa on (pessoa.fk_endereco_id_endereco = endereco.id_endereco)
    where cidade = 'Vitoria'  

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
    a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)

    SELECT * FROM funcionario f1, funcionario f2
    WHERE f1.fk_pessoa_id_pessoa = f2.fk_pessoa_id_pessoa
    ORDER BY f1.fk_pessoa_id_pessoa;

    b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

    SELECT * FROM pessoa p1, pessoa p2
    WHERE p1.id_pessoa = p2.id_pessoa
    ORDER BY p1.id_pessoa;

    SELECT * FROM pessoa p1, pessoa p2
    WHERE p1.nome = p2.nome AND
    p1.cpf = '177456749-98'
    ORDER BY p1.id_pessoa;

    SELECT * FROM servico s1, servico s2
    WHERE s1.tipo_servico = s2.tipo_servico
    ORDER BY s1.valor;

    SELECT * FROM ordem_servico os1, ordem_servico os2
    WHERE os1.status = os2.status
    ORDER BY os1.data;

    SELECT * FROM ordem_servico os1, ordem_servico os2
    WHERE os1.data = os2.data
    ORDER BY os1.status;

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


