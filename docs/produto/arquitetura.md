# Documento de Arquitetura

O EuPescador é um aplicativo mobile (para os pescadores) e web (para administração) cuja finalidade principal é permitir a criação, edição, validação e exportação de relatórios de campo sobre espécies de peixes nativas do estado do Tocantins, Brasil. O objetivo principal do aplicativo é o levantamento e recolhimento de dados científicos de tais espécies para pesquisadores da região. Neste documento serão exploradas todas as estruturas necessárias para o funcionamento do aplicativo e sua devida arquitetura.

Esse documento está em evolução, ele foi começado faz uns semestres, e tem como finalidade apresentar uma visão arquitetural do projeto EuPescador, facilitando dessa forma o entendimento do funcionamento dos processos envolvidos, aqui possui atualizações em relação ao documento de arquitetura produzido no semestre passado [2022-1](https://fga-eps-mds.github.io/2022-1-EuPescador-Doc/docs/produto/documento-arquitetura/). Com isto, esse documento estará descrevendo os componentes, as estruturas e as tecnologias envolvidas no funcionamento do sistema.

## Tecnologias

**Node.js**

O Node.js é um ambiente de execução JavaScript server-side, permitindo criar aplicações JavaScript para rodar como uma aplicação standalone em uma máquina, não dependendo de um browser para a execução. Aqui nesse site possui mais explicações sobre sua definição, características e vantages: [Link](https://www.alura.com.br/artigos/node-js-definicao-caracteristicas-vantagens-usos).

**PostgreSQL**

PostgreSQL é um sistema gerenciador de banco de dados objeto relacional de código. Possui características modernas como consultas complexas, chaves estrangeiras, tiggers, views e integridaded transicional. Aqui nesse site possui uma melhor explicação dessa tecnologia: [Link](https://4linux.com.br/o-que-e-postgresql/#:~:text=O%20PostgreSQL%20%C3%A9%20um%20descendente,%2C%20views%2C%20triggers%2C%20etc.).

**React Native**

React Native é uma framework baseada no Javascript que tem como finalidade facilitar o desenvolvimeto de aplicações mobiles multiplataformas. Aqui nesse link possui uma melhor explicação dessa framework: [Link](https://www.alura.com.br/artigos/react-native).

**React**

React é uma biblioteca baseada no Javascript que tem como finalidade auxiliar na criação de interfaces para aplicações web, lançada e mantida pelo Facebook. Aqui nesse link explica o que é e como funciona o React: [Link](https://www.hostinger.com.br/tutoriais/o-que-e-react-javascript#:~:text=O%20React%20%C3%A9%20uma%20biblioteca,Model%2DView%2DController).

**Docker**

Docker é uma ferramenta para gerar um ambiente isolado e construído especificamente para a equipe que será utilizado para facilitar o desenvolvimento do projeto. Nesse link explica melhor sobre como funciona o Docker: [Link](https://www.alura.com.br/artigos/comecando-com-docker).

**Heroku**

A Heroku é uma plataforma nuvem que faz deploy de várias aplicações back-end e front-end seja para hospedagem, testes em produção ou escalar aplicações, também possui integração com o Github. Nesse link explica quase todos os aspectos sobre o Heroku: [Link](https://blog.back4app.com/pt/o-que-e-o-heroku/).

## Diagrama

[![Arquitetura][2]][1]

[1]: ../assets/produto/Arquitetura.png 'Clique para ampliar'
[2]: ../assets/produto/Arquitetura.png

A representação da arquitetura do projeto, foi desenvolvido na ferramenta chamada [Lucid.app](https://lucid.app/users/login#/login)

**Fish Log**

Esse microsserviço é responsável por tudo que é relacionado aos relatórios de peixes, desde a criação do relatório pelo pescador até a validação pelo pesquisador. Além disso, esse serviço permitirá ao pescador e ao pesquisador editar ou remover relatórios pendentes.

**Fish Wiki**

Esse microsserviço é responsável pelo armazenamento de dados sobre Peixes, adquiridos a partir do consumo de uma planilha de informações disponibilizada pelos pesquisadores, a fim de fornecer conhecimentos que ajudem os pescadores a fazerem relatórios mais exatos.

**User**

Esse microsserviço é responsável pelo gerenciamento de usuários na plataforma, como a criação e a diferenciação de tipos de usuários: Pescadores e Pesquisadores.

**Client**

Onde tem a aplicação web e mobile. O web fica com a total gerência do projeto, e a parte mobile fica ao uso do pescador.

## Restrições Arquiteturais

### Escalabilidade
Atualmente temos uma restrição na versão mobile, onde todas as imagens do aplicativo carregam de uma vez, e como essas imagens são pesadas, acaba usando bastante a internet do usuário, e pesando também o banco de dados. A solução que encontramos foi paginar o banco de dados e ir mostrando as imagens no aplicativo conforme o pescador for dando o scroll, para não carregar as imagens de uma vez ao abrir a aplicação.

### Segurança
Como é um aplicativo sobre pesca, onde o pescador coloca dados sobre o peixe, sua localização e suas características, a preocupação da aplicação é não mostrar a localização exata, para evitar o aumento de caças e a extinção das expécies. Por tanto, o sistema alterada a localização das espécies alguns metros para evitar que isso ocorra.

### Usabilidade
Uma restrição em relação a usabilidade é, como a grande maioria dos lugares onde existe a pesca, a conexão com a internet acaba sendo ruim, a solução encontrada para driblar esse problema foi adicionar um aplicativo com funcionalidades offlines para que o pescador não tenha problemas ao utilizar o aplicativo.

## Referências

> Documento de Arquitetura. Eu_Pescador. Disponível em: [documento de arquitetura 2021.2](https://fga-eps-mds.github.io/2021-2-Eu_Pescador-Doc/#/Product/ArchitectureDocument). Acesso em: 10 dez. 2022.

> Definições Arquiteturais. Disponível em: [documento de arquitetura 2022.1](https://fga-eps-mds.github.io/2022-1-EuPescador-Doc/docs/produto/documento-arquitetura/). Acesso em: 10 dez. 2022.

## Versionamento

|    Data    | Versão |      Descrição       |                   Autor                   |
| :--------: | :----: | :------------------: | :---------------------------------------: |
| 10/12/2022 |  1.0   | Criação do documento | [Emily Dias](https://github.com/emysdias) |
| 05/01/2023 |  1.1   | Ajustes do documento | [Emily Dias](https://github.com/emysdias) |
