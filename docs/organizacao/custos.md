# Gerenciamento de Custos

O gerenciamento de custo é uma atividade de planejamento de um projeo que visa calcular os gastos sobre diferentes óticas do produto. Dessa maneira O gerenciamento dos custos do projeto inclui os processos envolvidos em planejamento, estimativas,
orçamentos, financiamentos, gerenciamento e controle dos custos, de modo que o projeto possa ser terminado
dentro do orçamento aprovado.

Para a realização dos cálculos aqui presentes foi utilizado dados reais que podem ser acessados ao fim e ao longo desse documento.

## Planilha de Custo

<iframe width="100%" height="480px" style={{minWidth: "640px", minHeight: "480px", backgroundColor: "#f4f4f4", border: "1px solid #efefef" }} src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRt3W0YYz4LlWMM6L0JB4nK5wqNcn3J3j71pNbHtIQl1M_AIEib13FaOlMyTCUuUWK6rHRB9-matrMN/pubhtml?widget=true&amp;headers=false"></iframe>

### Custo de Investimento

#### Equipamentos

O custo de equipamentos se refere à valor gasto para garantir que toda a equipe possua uma máquina capaz de rodaz a aplicação de forma adequada. Levando em consideração o tamanho do produto e a quantidade de serviços que são necessários para rodá-lo foi escolhido um [notebook com processador Intel I5 de décima primeira geração com 16 GB de memória RAM e 256GB de armazenamento](https://imgur.com/a/u7qOk2g).
> ```Custo do Notebook``` * ```Número de integrantes``` = ```R$ 40.920,00```

#### Infraestrutura

O custo relacionado à infraestrutura é aquele que é separado para a alocação de servidores remotos para a realização do deploy da aplicação. O serviço utilizado para a implantação vai ser o Heroku que tem uma cobrança mensal de 5 doláres. Com isso podemos calcular o valor mensal dos servidores:

> ```Número de servidores``` * ```Valor do servidor``` = ```40 dólares/mês```

Além disso, para a publicação do aplicativo na Playstore do celulares Android também é necessário o pagamento único de 25 dólares.

### Custo de Equipe

Segundo o [Jornal da USP](https://jornal.usp.br/artigos/a-cobranca-de-mensalidades-nas-universidades-publicas/) um aluno de uma universidade pública custa em média R$ 40.900 ao ano para os cofres públicos. Dessa forma, para sabermos o valor semanal de um aluno de uma universidade pública podemos calcular da seguinte maneira:
> ```Valor de um aluno universitário anualmente/(12*4)``` = ```R$ 852,00```

### Custos Extras

**Energia Elétrica**: Para o cálculo da energia elétrica é necessário saber que o [custo médio por kWh no DF](https://brasil61.com/n/valor-da-energia-eletrica-teve-alta-de-11-7-no-df-entre-2020-e-2021-pind223131) é de R$ 0,57/kWh e que de acordo com as especificações do notebook escolhido, ele possui um consumo médio de 0.065Wh. Dessa maneira, podemos calcular o valor médio de um uso de 6 horas da seguinte maneira:

> ```6 horas do computador ligado``` * ```Energia gasta por hora``` * ```Preço do kWh no DF```

E para calcular o custo semanal fazer:

* ```Custo diário``` * ```Número de dias uteis/4```  * ```Número de integrantes```  

**Internet**: Para o cálculo do gasto com internet foi utilizado um [comparador de planos](https://planos.minhaconexao.com.br/internet-banda-larga) de operadoras de banda larga. Por fim, foi escolhido o valor de R$ 120 que é capaz de pagar por planos de até 300 MB que são suficientes para garantir um bom acesso e uso da internet.

Com isso o custo mensal com internet pode ser dado por:

> ```Valor médio da internet no DF``` * ```Número de integrantes``` = ```Custo Mensal com Internet```



## Estimativas

### Custo da Atividade

O projeto será desenvolvido no decorrer de 5 sprints com 6 horas semanais dedicadas por cada estudante. De acordo com o agregador de vagas "[Vagas](https://www.vagas.com.br/cargo/estagiario-em-desenvolvimento-de-software)", o custo médio de um estagiário na área de desenvolvimento de sofwtare é de R$1.341,00. Dessa forma podemos fazer o cálculo da hora média de um estagiário:

> ```1341,00``` / ``` 20 dias uteis no mês ``` / ``` 6 horas diárias``` = ```R$10,91/hora```

Dessa forma também podemos calcular o custo de uma atividade:

> ```Tempo gasto (em minutos)``` * ``` Número de integrantes``` * ```Hora média de um estagiário / 60``` = ```Custo de uma atividade``` 

Estas estimativas serão realizadas em cada planejamento semanal, e poderão ser visualizadas na seguinte planilha:

<iframe width="100%" height="480px" style={{minWidth: "640px", minHeight: "480px", backgroundColor: "#f4f4f4", border: "1px solid #efefef" }} src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTmfl8hJACvmt0mmLYiaX7qct2TRANyr5INkW4eM9-MDhyLmcBjq7QfDHliXfjB7nUbBBB7rETzbf0R/pubhtml?widget=true&amp;headers=false"></iframe>

## Referências

> PMI. Um guia do conhecimento em gerenciamento de projetos. Guia PMBOK 5a. ed. - EUA: Project Management Institute, 2013.

> A cobrança de mensalidades nas universidades públicas. Jornal da USP. 17 abr, 2020. Acessado em: 08 Dez, 2022 Disponível em: 
https://jornal.usp.br/artigos/a-cobranca-de-mensalidades-nas-universidades-publicas/

> Estagiário em Desenvolvimento de Software. Vagas. Acessado em: 08 Dez, 2022 Disponível em: https://www.vagas.com.br/cargo/estagiario-em-desenvolvimento-de-software

> Valor da energia elétrica teve alta de 11,7% no DF entre 2020 e 2021. Brasil 61. 22 de Fevereiro de 2022. Acesso em 08 Dez, 2022 Disponível em: https://www.vagas.com.br/cargo/estagiario-em-desenvolvimento-de-software

## Versionamento

|    Data    | Versão |       Descrição       |                  Autor                   |
| :--------: | :----: | :-------------------: | :--------------------------------------: |
| 08/12/2022 |  1.0   | Criação do documento  |  [Washington](https://github.com/WashingtonBispo)|