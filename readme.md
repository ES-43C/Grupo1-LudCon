
![Capa - LudCon](Img/Capa.png)

# Projeto Disciplina: Requisitos de Software

Olá! Este repositório faz parte do projeto da disciplina de Requisitos de Software da UTFPR - Campus Cornélio Procópio 

## 1 Introdução

### 1.1  Nome do Grupo

*LudoTech Solutions* O Grupo é composto por:

- José Samuel;
- Ana Moreira;
- Alexandre de Lucas;
- Douglas Nascimento; e
- Matheus Oliveira.

### 1.2  Nome do Sistema

O Nome do Sistema é **LudCon**

### 1.3  Propósito do Sistema

Este documento apresenta os requisitos dos usuários a serem desenvolvidos pela *LudoTech Solutions*, fornecendo aos desenvolvedores as informações necessárias para o projeto e implementação, assim como para a realização dos testes e homologação do sistema.

O objetivo do sistema *LudCon* é através de um sistema de controle, permitir ao projeto de extensão Lúdico, o controle de jogos e sessões

### 1.4  Público Alvo

O público-alvo do software LudCon são os membros da comunidade acadêmica da UTFPR, principalmente os alunos, e demais usuários vinculados ao projeto de extensão Lúdico Em termos de faixa etária, o sistema abrange as diversas faixas etárias, mas como foco no público jovem.

### 1.5 Descrição dos usuários

#### 1.5.1 Administrador:

- Descrição: Perfil destinado aos membros da equipe organizadora do projeto Lúdico, responsáveis pela gestão da plataforma.
- Capacidades: Gerencia o catálogo de jogos (cadastrar, editar, remover), administra os usuários e tem permissão para visualizar relatórios de uso e cancelar qualquer reserva, se necessário.

#### 1.5.2 Utilizador:

- Descrição: Perfil padrão para qualquer participante da comunidade acadêmica que deseja utilizar os jogos do acervo.
- Capacidades: Realiza cadastro e login, busca jogos no catálogo, efetua e gerencia suas próprias reservas, e avalia os jogos que utilizou.

#### 1.5.3 Personas

> 🔗 [Acesse aqui](Docs/PersonasdeUsuario.pdf) | Personas de Usuário

#### 1.5.4 - Cenário Atual (Pré-Sistema)
O processo de gerenciamento de jogos e reservas é predominantemente manual, resultando em ineficiências e dificuldades para organizadores e participantes.

- Processo Manual:
  - A organização dos jogos e horários é feita em planilhas e grupos de WhatsApp.
  - As reservas são solicitadas e confirmadas informalmente por troca de mensagens.
  - Ferramentas Utilizadas:
  - Planilhas (Excel/Google Sheets).
  - Grupos de WhatsApp.
  - Listas impressas e anotações em papel.

- Principais Dificuldades:

  - Falta de uma fonte de informação centralizada e em tempo real sobre a disponibilidade dos jogos.
  - Alto risco de conflitos de agendamento e falhas de comunicação.
  - Inexistência de um método prático para registrar a frequência de uso ou as avaliações dos jogos.
  - Ilustração do Cenário Atual:

**Cenário (Pré-Sistema):** Júlia, monitora do projeto, controla o acervo de jogos através de uma planilha e de um grupo no WhatsApp Pedro, um estudante, envia uma mensagem para reservar o jogo Codenames Como Júlia está sem acesso à planilha no momento, ela não consegue confirmar a disponibilidade Confiando que estaria livre, Pedro vai até o local, mas descobre que outro grupo já havia reservado o jogo informalmente A situação gera frustração para ambos e sobrecarga de trabalho para Júlia, que precisa resolver o conflito na hora.

#### 1.5.5 - Cenário Proposto (Pós-Sistema)

- Processo Automatizado com o LudCon:

  - O administrador gerencia o catálogo de jogos e acompanha as reservas em um painel centralizado.
  - O usuário consulta a disponibilidade, realiza a reserva e avalia os jogos de forma autônoma pela plataforma.

- Componentes da Solução:
  
  - Plataforma web responsiva.
  - Banco de dados centralizado.
  - Sistema de permissões por perfil de usuário.
  - Benefícios e Novas Capacidades:
  - Navegação intuitiva para consulta, reserva e avaliação de jogos.
  - Autonomia e confiança para o usuário, com confirmações automáticas e visão clara dos horários.
  - Geração de dados estruturados (histórico de uso, avaliações) para apoiar a tomada de decisão dos administradores.
  - Ilustração do Cenário Proposto:

**Cenário (Pós-Sistema):** Agora, Júlia utiliza o painel administrativo do LudCon para manter o catálogo de jogos sempre atualizado Pedro acessa o sistema pelo seu celular, busca por Codenames, verifica os horários livres e reserva o jogo com um clique, recebendo uma confirmação instantânea Após a sessão, ele acessa a plataforma novamente para deixar sua avaliação O processo ocorre sem atritos, os conflitos são eliminados e Júlia pode, ao final da semana, exportar um relatório de uso para planejar as próximas atividades do projeto.

---


## 2 Documentos gerais no repositório

### 2.1 Requisitos Funcionais

| Identificador | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- |
| RF01 | O sistema deve permitir que um usuário se cadastre (com nome, e-mail, senha) e realize autenticação (login) | C |  
| RF02 | O sistema deve permitir que um Administrador cadastre jogos, informando no mínimo: nome, descrição e categoria | M | RF01 - RF10 |
| RF03 | O sistema deve apresentar aos usuários autenticados um catálogo para visualização dos jogos disponíveis | C | RF01 |
| RF04 | O sistema deve permitir que um Utilizador autenticado reserve um jogo para um dia e horário específicos | M | RF03 |
| RF05 | O sistema deve permitir que um Utilizador visualize e cancele suas próprias reservas futuras | M | RF04 |
| RF06 | O sistema deve permitir que um Utilizador avalie (com nota e/ou comentário) um jogo que ele já utilizou | S | RF04 |
| RF07 | O sistema deve impedir que uma reserva seja confirmada se o horário para o jogo selecionado já estiver ocupado | M | RF04 |
| RF08 | O sistema deve fornecer uma função de busca que permita filtrar o catálogo de jogos, no mínimo, por nome | S | RF03 |
| RF09 | O sistema deve exibir para o Utilizador uma seção de sugestões baseada nas categorias de jogos já reservados | S | RF04 - RF06 |
| RF10 | O sistema deve implementar um controle de acesso baseado em dois perfis: Administrador e Utilizador | C | RF01 |

### 2.2 Requisitos Não Funcionais

| Identificador | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- |
| RNF01 | O sistema deve garantir que a página inicial (homepage) seja acessível a partir de qualquer outra tela, por meio de um link ou botão claramente identificável. | S | RF01 |
| RNF02 | A interface do sistema deve ser suficientemente intuitiva para que um novo usuário consiga realizar as operações básicas (busca, reserva, avaliação) sem necessidade de treinamento formal. | M | RF01, RF02, RF03, RF04 |
| RNF03 | O tempo de resposta para ações interativas críticas (ex: login, busca, confirmação de reserva) não deve exceder 2 segundos em condições normais de rede. | M | RF01, RF04, RF06 |
| RNF04 | O sistema deve suportar um mínimo de 80 sessões de usuário simultâneas sem apresentar degradação de performance perceptível pelo usuário. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF05 | O sistema deverá oferecer integração com o Google Agenda, permitindo que o usuário adicione automaticamente a reserva ao seu calendário pessoal após a confirmação. | W | RF04 |
| RNF06 | O sistema deve manter uma disponibilidade (uptime) de, no mínimo, 98% durante os horários de funcionamento estabelecidos pelo projeto Lúdico. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF07 | Para garantir a recuperabilidade em caso de falha, o sistema deve realizar backups automáticos do banco de dados em intervalos não superiores a 12 horas. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF09 | O sistema deve ser compatível com as versões mais recentes dos navegadores web modernos (Google Chrome, Mozilla Firefox, Microsoft Edge) e possuir um design responsivo. | M | RF01 |
| RNF10 | Sendo uma aplicação web, o sistema deve funcionar corretamente nos navegadores suportados (RNF09), independentemente do sistema operacional do cliente (Windows, macOS, Linux, Android, iOS). | M | RF01 |
| RNF11 | O sistema deve estar em conformidade com as políticas e diretrizes de TI e de projetos de extensão da UTFPR, incluindo normas de segurança e acessibilidade. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF12 | O sistema deve ser projetado para que sua administração e manutenção possam ser realizadas pelos próprios membros do projeto de extensão, sem exigir conhecimento técnico aprofundado. | C | RF10 |
| RNF13 | A implementação do sistema está restrita à seguinte pilha tecnológica: Backend em Java com Spring Boot, Frontend em TypeScript com Angular e Banco de Dados PostgreSQL. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF14 | O processo de desenvolvimento do projeto deverá seguir a metodologia ágil Scrum. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF15 | Todo acesso a funcionalidades restritas do sistema deve ser precedido por um processo de autenticação de usuário (login e senha) bem-sucedido. | M | RF01 |
| RNF16 | O sistema deve garantir a segurança e a privacidade dos dados pessoais dos usuários, em conformidade com os princípios da Lei Geral de Proteção de Dados (LGPD). | M | RF01, RF10, RF05 |
| RNF17 | Devem ser gerados e armazenados logs de auditoria para eventos críticos, como tentativas de login (sucesso e falha), alterações de dados e outras ações administrativas. | M | RF01, RF10 |
| RNF18 | A arquitetura do software deve ser modular, desacoplando as principais funcionalidades (ex: gestão de usuários, jogos, reservas) para facilitar a manutenção e futuras evoluções. | S | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF19 | O código-fonte deve aderir a um guia de estilo e boas práticas de desenvolvimento consistentes, incluindo a documentação de componentes complexos. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |

### 2.3 Perguntas*

- **Sobre o funcionamento atual**
  - Como vocês controlam os jogos disponíveis e os horários de uso?
  - Há alguma ferramenta ou método que utilizam para esse controle?
  - Quem é responsável por manter essas informações atualizadas?

- **Dificuldades enfrentadas**
  - Quais são os principais problemas na organização dos encontros?
  - Já houve conflitos de horário ou uso de jogos? Como foram resolvidos?
  - É difícil saber quem participou das sessões?

- **Perfis e permissões**
  - Quais tipos de usuários participam do projeto?
  - Que ações diferentes cada perfil deveria ter no sistema?
  - Quem pode autorizar, cancelar ou bloquear reservas?

- **Reservas e agendamentos**
  - É importante poder agendar jogos com antecedência?
  - Preferem horários fixos ou flexíveis para as reservas?
  - Os usuários devem poder editar suas próprias reservas?

- **Informações e relatórios**
  - Que dados vocês gostariam de acompanhar no sistema?
  - Devem ser registradas a frequência de uso e participação?
  - Relatórios são úteis para o planejamento? Quais?

- **Funcionalidades desejadas**
  - Que funcionalidades seriam mais úteis para o sistema?
  - O que não pode faltar de jeito nenhum?
  - Avaliações de jogos pelos usuários seriam úteis?

- **Considerações finais**
  - Existe alguma regra ou limitação que o sistema precisa seguir?
  - Algo mais que gostariam de incluir?

### 2.4 Entrevista

> 🔗[Acesse aqui](https://drive.google.com/file/d/16iVjAabSYFPvGYE_7LZFbWzFgqTazPct/view?usp=sharing) | Vídeo da Entrevista

> 🔗[Acesse aqui](Docs/Transcicao) | Transcrição da Entrevista

### 2.5 Histórias do Usuário

01. Como um novo participante, quero me cadastrar no sistema usando meu nome, e-mail e uma senha, para que eu possa criar um perfil e acessar a plataforma.
02. Como um participante, quero visualizar um catálogo com todos os jogos disponíveis, exibindo seus nomes e imagens, para que eu possa explorar as opções e escolher qual quero jogar.
03. Como um participante, quero usar uma barra de busca para encontrar um jogo específico pelo nome, para que eu possa localizar rapidamente o item que desejo.
04. Como um participante, quero selecionar um jogo e escolher um dia e horário disponíveis em um calendário, para que eu possa garantir o uso do jogo sem conflitos.
05. Como um participante, quero acessar uma área de "Minhas Reservas" para visualizar e poder cancelar agendamentos futuros, para que eu tenha controle e possa liberar o horário caso meus planos mudem.
06. Como um participante, quero avaliar um jogo que já utilizei, atribuindo uma nota de 1 a 5 estrelas e um comentário opcional, para que eu possa compartilhar minha opinião e ajudar outros usuários a escolherem.
07. Como um participante, quero ver uma seção de "Recomendados" na página inicial, baseada nos tipos de jogos que já reservei, para que eu possa descobrir novos jogos que se alinhem ao meu gosto.
08. Como um administrador, quero ter um painel para gerenciar todo o ciclo de vida dos jogos, para que eu possa manter o catálogo do projeto sempre atualizado.
09. Como um administrador, quero adicionar um novo jogo ao sistema, informando seu nome, descrição e categoria, para que ele fique disponível para reserva pelos participantes.
10. Como um administrador, quero ter a permissão de cancelar qualquer reserva existente no sistema, para que eu possa resolver conflitos de horário ou gerenciar a indisponibilidade de um jogo.
11. Como um usuário, quero ter um menu de navegação sempre visível e claro, para que eu possa me locomover entre as seções principais de forma rápida e prática.
12. Como um novo usuário, quero conseguir entender como fazer uma reserva sem precisar de um manual ou tutorial, para que minha primeira experiência com o sistema seja positiva.
13. Como um usuário, quero que as páginas carreguem em poucos segundos e que as ações aconteçam de forma instantânea, para que eu não perca tempo e sinta que o sistema é eficiente.
14. Como um usuário, quero ter a certeza de que meus dados pessoais estão seguros e são tratados conforme a LGPD, para que eu possa confiar na plataforma e usá-la com tranquilidade.
15. Como um administrador, quero que o sistema registre quem realizou as ações administrativas importantes (logs), para que seja possível rastrear e auditar eventos em caso de algum problema.

### 2.6 Diagramas de Caso de Uso e Especificações

> 🔗[Acesse aqui](Docs/casoDeUso) | Diagrama de Caso de Uso

### 2.7 Diagramas de Atividades

> 🔗[Acesse aqui](https://github.com/user-attachments/assets/58849a7a-db5a-453c-a735-48f744c754b2) | Diagrama de Atividades

### 2.8 Diagrama de Classes 

> 🔗[Acesse aqui](Docs/Classes) | Diagrama de Classes

### 2.9 Matrizes de Rastreabilidade

- Matriz de Rastreabilidade: Requisitos Funcionais vs. Histórias de Usuário

| Requisito Funcional                       | HU01 | HU02 | HU03 | HU04 | HU05 | HU06 | HU07 | HU08 | HU09 | HU10 |
| :---------------------------------------- | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| RF01 - Cadastrar e autenticar usuário     |   X  |      |      |      |      |      |      |      |      |      |
| RF02 - Cadastrar jogos (Admin)            |      |      |      |      |      |      |      |   X  |   X  |      |
| RF03 - Apresentar catálogo de jogos       |      |   X  |      |      |      |      |      |      |      |      |
| RF04 - Reservar jogo                      |      |      |      |   X  |      |      |      |      |      |      |
| RF05 - Cancelar próprias reservas         |      |      |      |      |   X  |      |      |      |      |      |
| RF06 - Avaliar jogo utilizado             |      |      |      |      |      |   X  |      |      |      |      |
| RF07 - Impedir reserva em horário ocupado |      |      |      |   X  |      |      |      |      |      |      |
| RF08 - Buscar jogo por nome               |      |      |   X  |      |      |      |      |      |      |      |
| RF09 - Exibir sugestões de jogos          |      |      |      |      |      |      |   X  |      |      |      |
| RF10 - Controle de acesso (Perfis)        |   X  |      |      |      |      |      |      |   X  |   X  |   X  |

- Matriz de Rastreabilidade: Requisitos Não Funcionais vs. Histórias de Usuário

| Requisito Não Funcional               | HU01 | HU02 | HU03 | HU04 | HU05 | HU06 | HU07 | HU08 | HU09 | HU10 | HU11 | HU12 | HU13 | HU14 | HU15 |
| :------------------------------------ | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| RNF01 - Navegabilidade |      |      |      |      |      |      |      |      |      |      |   X  |      |      |      |      |
| RNF02 - Usabilidade|      |   X  |      |   X  |      |   X  |      |      |      |      |   X  |   X  |      |      |      |
| RNF03 - Desempenho |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |      |      |      |   X  |      |      |
| RNF06 - Confiabilidade |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |
| RNF07 - Recuperabilidade |   X  |      |      |   X  |   X  |   X  |      |   X  |   X  |   X  |      |      |      |      |      |
| RNF09 - Compatibilidade |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |      |   X  |      |
| RNF12 - Manutenibilidade |      |      |      |      |      |      |      |   X  |   X  |   X  |      |      |      |      |      |
| RNF15 - Segurança |      |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |   X  |      |      |      |      |      |
| RNF16 - Segurança |   X  |      |      |      |      |      |      |      |      |      |      |      |      |   X  |      |
| RNF17 - Segurança |   X  |      |      |      |      |      |      |   X  |   X  |   X  |      |      |      |      |   X  |


## 3 Protótipos

> 🔗[Acesse aqui](Docs/Proto) | Descrição dos Protótipos
