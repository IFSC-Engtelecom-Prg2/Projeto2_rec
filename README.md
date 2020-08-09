# Projeto 2: Analisador financeiro

O projeto 2 tem por objetivo desenvolver um programa que analise ativos financeiros da [Bolsa de Valores de São Paulo](http://www.b3.com.br/pt_br/), para identificar os ativos com melhor razão entre retorno e risco. Mais especificamente, o programa deve ser capaz de apresentar:
* Os N ativos com maior retorno financeiro em um determinado período
* A rentabilidade de uma carteira de investimentos composta por um conjunto de ativos

A análise deve ser feita com base no [arquivo de dados disponibilizado](http://tele.sj.ifsc.edu.br/~msobral/prg2/2018-2/dados.zip). Esse arquivo de dados possui cotações de ativos entre janeiro de 2007 e setembro de 2018, e suas possuem linhas este formato:

```
mes/ano nome_do_ativo valor_em_R$
```

Ex:

```
01/2007 ALLL3 8.0
01/2007 ALLL4 3.68
```

Seu programa deve receber do usuário estas informações:
* Período de análise, na forma de um mês  e ano inicial, e mês e ano final (ex: 01/2018 a 08/2018)
* O tipo de análise a ser realizada
* A quantidade de ativos cujos resultados devem ser apresentados (parâmetro N), quando pertinente para a análise
* Os nomes dos ativos que compõem a carteira cuja rentabilidade deve ser calculada, quando pertinente para a análise

Seu programa deve obrigatoriamente usar tabela hash para extrair e organizar os dados durante a análise. Mas você deve perceber que sem a tabela hash a tarefa ficaria mais complicada ...

Seu programa pode ler os arquivos de dados UMA ÚNICA VEZ, independente da quantidade de análises a serem realizadas. Todos os dados necessários devem ser lidos e armazenados de forma conveniente em memória. As análises devem ser efetuads sobre esses dados em memória.

Algumas informações são apresentadas a seguir para esclarecer os elementos da análise a ser realizada.

## Retorno financeiro

O retorno financeiro é definido como a porcentagem que expressa o aumento no valor de um ativo em um determinado período. Por exemplo, se em 1/1/2018 um ativo valia R$ 10,00, e em 1/7/2018 esse mesmo ativo vale R$ 12,10, então o retorno financeiro nesse período foi de 21%. De forma geral, o retorno de um ativo pode ser calculado assim:

Y = (Vf - Vi) / Vi x 100%

... sendo Y o retorno financeiro, Vf o valor no final do período analisado e Vi o valor no início desse período.


## Referências
    
* [Estatísticas sobre Tesouro Direto](http://www.tesouro.gov.br/-/balanco-e-estatisticas)
* [Séries históricas de ativos negociados na Bovespa](http://www.b3.com.br/pt_br/market-data-e-indices/servicos-de-dados/market-data/historico/mercado-a-vista/series-historicas/)
* [Informações sobre as cotações históricas na Bovespa](http://www.b3.com.br/pt_br/market-data-e-indices/servicos-de-dados/market-data/historico/mercado-a-vista/cotacoes-historicas/)
