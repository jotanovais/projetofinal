# projetofinal# Feedback_360<sup>oTool

## 1. Apresentação

O Project Manager é um site voltado para organização e supervisão dos alunos, tendo a visão do aluno para as demandas e cronograma, e o professor tendo visão das entregas e atividades pendentes por parte do aluno.

## 2. Especificação Funcional

Os usuários devem ser previamente cadastrados, tendo dois tipos de cadastros, sendo o de aluno e professor, podendo então realizar o acesso ao dashboard, os alunos terão o cronograma de suas matérias e atividades.

![](https://github.com/jotanovais/projetofinal/blob/main/UseCase.png)

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

A figura 1 mostra a modelagem do banco de dados

![]()
<img src="https://github.com/jotanovais/projetofinal/blob/main/Screenshot.png" width="500">
> Figura 1. Modelagem do Banco de Dados


O cadastro é enviado ao MySql Server e é armazenado em diferentes tabelas, tendo como Primary Key o ID do aluno ou professor.

Como ferramentas e tecnologias de apoio ao processo de desenvolvimento temos:
- **Visual Studio**: editor de texto utilizado na geração da base de código da aplicação;
- **MySQL Server**: Banco de Dados oriundo da Oracle; 
- **Figma**: Site para criação e prototipação de tela;
- **Git**: sistema distribuído de controle de versão de software.
- **HTML, CSS e JavaScript**: para desenvolvimento e estilização dos componentes

### 4. Resultados

A figura 3 mostra a tela de cadastro do aluno. Nessa tela o aluno irá se cadastrar

<img src="https://github.com/jotanovais/projetofinal/blob/main/CadastroAluno.png" border="0" width="500">
> Figura 3. Tela de cadastro do aluno.


A figura 4 mostra o dashboard de atuação do aluno, com atividades enviadas ou não
![]()
<img src="https://github.com/jotanovais/projetofinal/blob/main/AtuacaoAluno.png" width="500">
> Figura 4. Atuação do Aluno.

A figura 5 apresenta as notas que o aluno obteve durante o bimestre ou semestre.

![]()
<img src="https://github.com/jotanovais/projetofinal/blob/main/Notas.png" width="500">
> Figura 5. Notas obtidas
