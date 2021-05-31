# projetofinal# Feedback_360<sup>oTool

## 1. Apresentação

O Project Manager é um site voltado para organização e supervisão dos alunos, tendo a visão do aluno para as demandas e cronograma, e o professor tendo visão das entregas e atividades pendentes por parte do aluno.

`<CodeProject>`[Development of a Tool to Support the 360 Feedback Process in Workgroups Using Vue.js and Firebase DBaaS](https://www.codeproject.com/Articles/5272992/Development-of-a-Tool-to-Support-the-360-Feedback "Development of a Tool to Support the 360 Feedback Process in Workgroups Using Vue.js and Firebase DBaaS")

`<ResearchGate>`[Development of a Tool to Support the 360 Feedback Process in Workgroups Using Vue.js and Firebase DBaaS](https://www.researchgate.net/publication/342852151_Development_of_a_Tool_to_Support_the_360_Feedback_Process_in_Workgroups_Using_Vuejs_and_Firebase_DBaaS "Development of a Tool to Support the 360 Feedback Process in Workgroups Using Vue.js and Firebase DBaaS")

## 2. Especificação Funcional

Os usuários devem ser previamente cadastrados, tendo dois tipos de cadastros, sendo o de aluno e professor, podendo então realizar o acesso ao dashboard, os alunos terão o cronograma de suas matérias e atividades.

![](https://www.codeproject.com/KB/applications/5272992/use_case_diagram.jpg)

##### Lista de Usuários

	 1. Administrador
	 2. Professor
	 3. Aluno

##### Principais Funcionalidades


- [x] Cadastrar-se
- [ ] Editar de perfil 
- [x] Criar salas para grupos
- [x] Gerenciar atividades
- [x] Consultar Cronograma


##### Perfis de Acesso

| FUNCIONALIDADE | Aluno | Professor | ADM |
| ------------ | ------------ | ------------ | ------------ |
| Cadastrar-se |  X |  X |   |
| Consultar e editar perfil | X |  X   | X |
| Postar Atividades |  |   X  |     |
| Alterar Cronograma |  |  X  |     |
| Enviar atividades | X  |   |   X  |
| Gerenciar cadastro de usuários |   |   |   X  |


##### Regras de Negócio

- **Aprovação**: Uma vez que o cadastro tenha sido feito pelo próprio usuário, o sistema irá avisar aos administradores a necessidade de aprovação dos perfis, bem como a alteração de acesso. Após todos os usuários serão livres para utilizar o sistema dentro de suas limitações.

- **Turmas**: Os administradores irão cadastrar as turmas, informando o nome, quem serão os professores e seus respectivos alunos;

- **Criação de Salas em Grupos**: Os professores poderão criar salas com pequenos grupos para monitorar atividades.

- **Perfis de acesso**: serão três perfis para cadastro no sistema, sendo estes os perfis de alunos, professores e administradores, cada um com seus níveis de acesso e responsabilidades sobre o sistema.

- **Cadastro**: os usuários são livres para fazer o próprio cadastro necessitando apenas informar o nome, telefone, e-mail e senha de preferência. Os demais dados pessoais podem ser preenchidos posteriormente ao primeiro acesso no sistema;

### 3. Projeto e Tecnologia Envolvida

Para o desenvolvimento do sistema a linguagem foram utilizadas as linguagens HTML, CSS, JAVASCRIPT e JAVA

Para armazenamento dos dados será utilizado MySQL Server, um banco de dados pertencente a Oracle

A figura 1 mostra os documentos e seus atributos definidos para o projeto. Vale ressaltar principalmente o conjunto de datos de configuração, composto por dados dinâmicos, tais como os "critérios de avaliação", "dados pessoais de um user" entre outros.

![]()
<img src="https://www.codeproject.com/KB/applications/5272992/tela_firebase_.png" width="500">
> Figura 1. Tela de gerenciamento do Firebase

As principais entidades que suportam o modelo do sistema desenvolvido são:

- **1. coleções para entidades de domínio**

	- **Alunos (users)**: Jovens que estão colocando a vida acadêmica em dia e sendo avaliados
  
	- **Professores (evaluations)**: Principal agente na hora de monitorar e postar atividades.

	

- **2. coleções para relacionamentos** e

	- **evaliations_rates**: link usado para indicar a participação da pessoa em um processo de avaliação
squad_user**: link para associar uma pessoa a uma tabela de taxas de seleção

- **3. coleções para espelhamento**

	- **data_de_avaliação**: replica as informações para melhorar a carga de trabalho de apresentação de dados, o portfólio do usuário e da equipe


A figura 2 mostra o escopo de dependência das entidades com uma abstração baseada em objetos e colaboração. 

<img src="https://i.ibb.co/q0JL539/asgoto-model-preview-1.png" alt="asgoto_model_preview_1" border="0" width="500">
> Figura 2. Modelo de entidades e suas colaborações.


A participação é enviada ao servidor de banco de dados por meio do Firebase Google API (Application Programming Interface). Esses dados serão salvos separadamente em diferentes coleções (**squads**) conectadas pelo ID dos membros avaliados e o ID da sessão de avaliação (**squad_user**). Portanto, a seguir, todas as outras classificações dos mesmos processos (**evaluations**) também são adicionadas.

Como ferramentas e tecnologias de apoio ao processo de desenvolvimento temos:
- **Visual Studio**: editor de texto utilizado na geração da base de código da aplicação;
- **Firebase**: plataforma de desenvolvimento mobile e web pertencente a Google, com diversos serviços, dos quais serão utilizados as API’s e o banco de cados; 
- **Vue JS**: biblioteca JavaScript utilizada para construção de interfaces de usuário baseadas em componentes;
- **Bulma**: framework visual compatível com linguagens web;
- **Adobe Photoshop CC 2020**: editor de imagens;
- **Git**: sistema distribuído de controle de versão de software.
- **HTML, CSS e JavaScript**: para desenvolvimento e estilização dos componentes

### 4. Resultados

A figura 3 mostra a principal tela do sistema. Nela um membro de um determinado time avalia seus pares (outros integrantes do time) de acordo com os critérios definidos durante a criação da sessão de avaliação (assessement).

<img src="https://i.ibb.co/wR9pC3R/asgoto-tela-avaliando-1.png" alt="asgoto_tela_avaliando_1" border="0" width="500">
> Figura 3. Tela do processo de avaliação.


A figura 4 apresenta dois momentos para o usuário administrador. Na primeira parte (topo) trata-se da tela de definiçao de uma sessão de avaliação (assessment). Nela o administrador define a identificação, as datas e as equipes que receberão esta sessão.

Na parte inferior, é apresentada a funcionalidade de construção de um time de trabalho. Trata-se de uma funcionalidade muito simples que ainda explora recursos de usabilidade para deixar a experiência do administrador mais agradável. Nesta tela o administrador define o nome do time, seu lider imediato e utilizando multiplas seleções inclui ou remove seus membros usuários.

![]()
<img src="https://www.codeproject.com/KB/applications/5272992/tela_admin.png" width="500">
> Figura 4. Tela do Administrador.

A figura 5 apresenta o relatório disponível para cada usuário. Ela tenta focar a atenção do usuário no contexto geral utilizando cores e um componente de fácil visualização estatística. Lembrando que as avaliações recebidas são anônimas.

![]()
<img src="https://www.codeproject.com/KB/applications/5272992/tela_relatorio_avaliacao_donut.png" width="500">
> Figura 5. Personal Rate Report Screen.

A figura 6 é a página de perfil do usuário. Além dos dados pessoais e a possibilidade de alterá-los o usuário também tem um indíce com sua pontuação geral no sistema, seguido do sua categoria.

![]()
<img src="https://www.codeproject.com/KB/applications/5272992/tela_home2.png" width="500">
> Figura 6. Personal Homepage from a Team Member.

### 5. Deploy

#### Para utilização do sistema:

1. Faça o clone deste projeto
2. Acesse a pasta web
3. Rode NPM INSTALL
4. Agora execute NPM RUN SERVE

Vale ressaltar que:

- Os cadastros devem ser feitos pela tela de registro
- Os usuários só terão acesso às avaliações se estiverem em uma equipe
- Ainda não foi implementado nenhuma tratativa para usuário desabilitado
- O acesso a base de dados firebase ainda é privado, envie um e-mail para o e-mail andreseijigoto@gmail.com para que seu e-mail seja incluído na lista editável

#### Project setup

	$ npm install

**Compiles and hot-reloads for development**

	$ npm run serve

**Compiles and minifies for production**

	$ npm run build

**Lints and fixes files**

	$ npm run lint


More and customize configuration: See [Configuration Reference](https://cli.vuejs.org/config/).
