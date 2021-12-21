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
    Pessoa,Funcionario,Serviço      
    C) Principais fluxos de informação/entidades do sistema (mínimo 3).
    Pessoa -> solicita -> serviço
    Funcionario -> executa -> ordem de serviço
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/Julymusso/Trab_BD1_2021_Barbearia_Gourmet/blob/master/images/Trabalho_1_Conceitual_v3.png?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


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
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

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


