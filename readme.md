
# Projeto Disciplina: Requisitos de Software

Olá! Este repositório faz parte do projeto da disciplina de Requisitos de Software da UTFPR - Campus Cornélio Procópio. 

Link do Padlet: https://padlet.com/josesamuel4/requisitos-ak7sijmoxmn7q0cj

## 1. Introdução

***1.1.  Nome do Grupo***

LudCon
- José Samuel;
- Ana Moreira;
- Alexandre de Lucas;
- Douglas Nascimento; e
- Matheus Oliveira.

***1.2.  Nome do Sistema***

**LudCon**

***1.3.  Propósito do Sistema***

Este documento apresenta os requisitos dos usuários a serem desenvolvidos pela *`Tiger's Digital`*, fornecendo aos desenvolvedores as informações necessárias para o projeto e implementação, assim como para a realização dos testes e homologação do sistema.'

O objetivo do sistema `LudCon` é *através de um sistema de controle, permitir ao projeto de extensão Lúdico, o controle de jogos e sessões*

***1.4.  Público Alvo***

O público alvo do software são membros e/ou usuários do Lúdico portanto jovens, adultos, idosos, crianças podem estar inclusos em questão de faixa etária.

***1.5. Descrição dos usuários***

Utilizadores: São os usuários que usam o software tanto para vizualizar e reservar hórario para se entreter e após o uso podem avaliar o jogo.

Administradores: São os usuários que configuram e organizam as funções que o software disponibiliza para os utilizadores.

***Personas:***

[Acesse aqui - Personas de Usuário](Docs/PersonasdeUsuario.pdf)

#### Situação Atual – Antes da Solução

**O que as pessoas fazem?**  
- Júlia (monitora) organiza manualmente a lista de jogos disponíveis e os horários das sessões, geralmente em planilhas e mensagens no WhatsApp.  
- Pedro (usuário) entra em contato por mensagens para perguntar sobre a disponibilidade e tenta reservar verbalmente ou via grupo de WhatsApp.

**Quais os artefatos envolvidos?**  
- Planilhas em Excel/Google Sheets  
- Grupos de WhatsApp  
- Impressões de listas de jogos  
- Anotações manuais em papel  

**O que elas precisam saber?**  
- Quais jogos estão disponíveis e em quais horários  
- Quem já reservou cada jogo  
- Se há conflitos de horário  
- Como registrar avaliações ou frequência dos participantes

---

#### Situação com a Solução – Depois da Implementação do LudCon

**O que as pessoas fazem?**  
- Júlia acessa o sistema LudCon via navegador, faz login como administradora e cadastra ou atualiza os jogos disponíveis. Ela gerencia permissões e visualiza reservas em tempo real.  
- Pedro acessa o sistema pelo celular, consulta os jogos disponíveis, faz uma reserva e recebe uma confirmação. Após jogar, ele avalia o jogo diretamente pela plataforma.

**Quais os artefatos envolvidos?**  
- Plataforma web responsiva (LudCon)  
- Banco de dados centralizado com registros de usuários, jogos, reservas e avaliações  
- Sistema de permissões por perfil  

**O que elas precisam saber?**  
- Como navegar pelo sistema  
- Como filtrar, cadastrar e editar jogos  
- Como realizar uma reserva e verificar status  
- Como acessar e interpretar relatórios (no caso da Júlia)

---

#### Cenário: Antes

Júlia é uma estudante engajada no projeto de extensão Lúdico e responsável por ajudar na organização das sessões de jogos. Ela utiliza planilhas no Google Drive e grupos de WhatsApp para controlar os jogos disponíveis e os horários de uso. Toda semana, Júlia precisa atualizar manualmente a planilha e responder mensagens dos colegas interessados em participar dos encontros.

Pedro, um estudante do 3º período de Engenharia da Computação, quer participar das atividades e pergunta no grupo se o jogo *Codenames* estará disponível na quinta-feira à tarde. Júlia confere a planilha, mas como não está com o notebook no momento, responde de forma genérica. Pedro então supõe que o jogo estará disponível e comparece no horário desejado, mas descobre que outro grupo já havia reservado informalmente o mesmo jogo.

A situação gera frustração. Júlia precisa reorganizar os horários em tempo real e lidar com vários pedidos simultâneos. Pedro se sente desmotivado por não conseguir jogar. Ao final do dia, Júlia atualiza a planilha com o que aconteceu, mas sem registros claros das reservas e sem avaliações dos jogos.

---

#### Cenário: Depois

Júlia é uma monitora ativa do projeto Lúdico e agora utiliza o sistema LudCon para organizar os jogos e horários das sessões. Ao acessar a plataforma pelo navegador, ela realiza login como administradora, cadastra os novos jogos recebidos e atualiza os horários disponíveis na agenda integrada.

Pedro acessa o sistema LudCon pelo celular e, ao navegar pela interface intuitiva, encontra uma lista com todos os jogos cadastrados. Ele utiliza o filtro por nome e localiza o *Codenames*. Ao verificar a disponibilidade, Pedro vê que o horário de quinta-feira às 16h está livre e faz sua reserva com um clique. Ele recebe uma notificação de confirmação imediatamente.

Durante o encontro, Pedro utiliza o jogo e, ao final, avalia sua experiência diretamente pelo sistema. Júlia acompanha todas as reservas e avaliações em tempo real pela interface administrativa. Ao final da semana, ela exporta um relatório com o histórico de uso e as avaliações dos jogos, o que facilita o planejamento de futuras sessões.

Com o uso do LudCon, os encontros se tornam mais organizados, os conflitos de horários são evitados automaticamente e tanto os participantes quanto os monitores têm mais controle e confiança sobre o funcionamento do projeto.

---


## 2. Documentos gerais no repositório

***2.1. Requisitos Funcionais***

| Identificador | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- |
| RF01 | O software deve permitir que o usuário faça cadastro e login no sistema. | M |  
| RF02 | O sistema deve permitir o cadastro de jogos. | M | RF01, RF10 |
| RF03 | O Software deve permitir ao usuário uma tela de visualização de jogos. | C | RF01, RF10, RF02 |
| RF04 | O software deve permitir ao usuário fazer uma reserva do jogo que deseja utilizar. | M | RF01, RF10, RF02, RF03 |
| RF05 | O sistema deve permitir ao usuário editar ou cancelar suas reservas de jogos. | M | RF01, RF10, RF02, RF03, RF04 |
| RF06 | O sistema deve permitir ao usuário avaliar os jogos utilizados. | S | RF01, RF10, RF02, RF03, RF04 |
| RF07 | O sistema deve permitir ao usuário não conflitar com outros horários marcados. | M | RF01, RF10, RF02, RF03, RF04, RF05 |
| RF08 | O sistema deve permitir ao usuário buscar jogos por meio de filtros (nomes, códigos, id). | S | RF01, RF10, RF02, RF03, RF04, RF06 |
| RF09 | O sistema deve permitir ao usuário visualizar suas preferências com base no histórico de jogos utilizados. | S | RF01, RF10, RF02, RF03, RF04, RF05, RF06, RF07 |
| RF10 | O sistema deve permitir ao usuário gerenciar ou  escolher seu nível de permissão com o software de acordo com seu tipo de usuário. | M | RF01 |

***2.2. Requisitos Não Funcionais***
| Identificador | Descrição | Prioridade | Depende de |
| --- | --- | --- | --- |
| RNF01 | O usuario deve ser capaz de acessar a homepage de qualquer outra parte. | S | RF01 |
| RNF02 | Deve ser intuitivo o suficiente para que qualquer estudante possa utilizá-lo sem necessidade de treinamento formal. | M | RF01, RF02, RF03, RF04 |
| RNF03 | O sistema deve responder às requisições do usuário em até 2 segundos para ações básicas (como login, reserva de jogos, avaliação). | M | RF01, RF04, RF06 |
| RNF04 | Deve suportar pelo menos 80 usuários simultâneos sem degradação significativa da performance. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF06 | O sistema deve estar disponível 98% do tempo durante os horários de funcionamento do projeto Lúdico. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF07 | Deve ser capaz de recuperar-se automaticamente de falhas simples sem perda de dados. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF09 | sistema deve ser acessível por navegadores modernos (Chrome, Firefox, Edge) e dispositivos móveis (responsivo). | M | RF01 |
| RNF10 | Deve funcionar tanto em sistemas operacionais Windows quanto Android/iOS. | M | RF01 |
| RNF11 | O sistema LudCon deve seguir as diretrizes de tecnologia da informação e extensão da universidade, respeitando normas de segurança, acessibilidade e uso de software institucional.  | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF12 | A administração do sistema será responsabilidade dos universitários envolvidos no projeto Lúdico, sob supervisão de um professor ou coordenador, garantindo que a manutenção e operação estejam alinhadas com os objetivos acadêmicos do projeto. | C | RF10 |
| RNF13 | O sitema deve ser feito na linguagem java. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF14 | O sistema deve ser produzido utilizando a metódologia SCRUM. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF15 | O acesso ao sistema deve ser controlado por autenticação de usuário (login e senha). | M | RF01 |
| RNF16 | Os dados pessoais dos usuários e administradores devem ser armazenados de forma segura, respeitando a LGPD. | M | RF01, RF10, RF05 |
| RNF17 | O sistema deve registrar logs de acesso e ações administrativas para auditoria. | M | RF01, RF10 |
| RNF18 | O sistema deve ser modular, facilitando alterações e atualizações futuras.  | S | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 |
| RNF19 | O código deve seguir boas práticas de desenvolvimento, com documentação básica e padronização. | M | RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF10 
| RNF20 | O Sistema precisa dar autonomia para os administradores cancelar as reservas. | W | RNF13 |
***2.3. Perguntas***

-Como é feito hoje o controle dos jogos disponíveis?

-Como vocês organizam as reservas de jogos ou horários?

-Existe alguma planilha ou sistema que vocês usam atualmente?

-Quais são os maiores problemas na organização dos encontros?

-Quem pode autorizar ou bloquear o uso de jogos?

-Quem são os tipos de usuários que usam o sistema? (monitor, aluno, prof...?)

-Quais permissões diferentes cada tipo de usuário deve ter?

-Como vocês controlam quem participou de cada evento?

-Como vocês decidem quais jogos estarão disponíveis em cada encontro?

-Já aconteceu de  grupos quererem o mesmo jogo ao mesmo tempo e não ter?

-É importante registrar a frequência de uso de cada jogo?

-Vocês acham importante que o sistema permita agendar jogos com antecedência?

-Vocês preferem horários fixos ou flexíveis para reservas?

-Quais dados vocês gostariam de extrair do sistema? (frequência, avaliações, histórico)

-Alguma funcionalidade que facilitaria muito o trabalho de vocês?

-Existe alguma limitação técnica ou regra da faculdade que precisamos seguir?

-O que o sistema não pode deixar de ter?

*<Arquivo com as perguntas realizadas na entrevista .>*

***2.4. Entrevista***

*<Arquivo com as respostas do indivíduo entrevistado e link do drive com upload da gravação.>*

***2.5. Histórias do Usuário***

*<Imagem, arquivo (PDF), link com as Histórias de Usuário.>*

***2.6. Diagramas de Caso de Uso e Especificações***

*<Imagem, arquivo (PDF), link com Diagrama de Caso de Uso.>*

***2.7. Diagramas de Atividades***

*<Imagem, arquivo (PDF), link com Diagrama de Atividades.>*

***2.8. Matrizes de Rastreabilidade***

*<Imagem, arquivo (PDF), link com Matriz de Rastreabilidade.>*

***2.9. Protótipos***

*<Imagem, arquivo (PDF), link com Protótipo.>*

## Referências

*<Esta seção é destinada à descrição das referências utilizadas pelo documento, como por exemplo, URLs e livros. Ver exemplo a seguir:>*

[1] “Glossário da _USina_”, <_id_doc glossário_>, Versão <_versão_>. Localização: <_localização_>.
