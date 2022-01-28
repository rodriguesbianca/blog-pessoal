---
date: "2021-01-01"
draft: false
excerpt: "Existe relação entre o perfil epidemiológico da população abordada com o seu grau de dependência à nicotina?"
subtitle: ""
title: Perfil epidemiológico de dependência nicotínica - Parte I
weight: 2
tags:
  - analise de dados
categories:
  - estágio supervisionado
  - visualização de dados
---

[logomarca]: pessoa-fumando.jpg
[fumando]: https://www.pexels.com/pt-br/foto/pessoa-fumando-cigarro-2827798/ "Foto de lilartsy no Pexel"

---

[![a logomarca do google][logomarca]][fumando]

## Contextualização 

#### Existe relação entre o perfil epidemiológico da população abordada com o seu grau de dependência à nicotina?

Foi com o objetivo de responder a essa pergunta que esse estudo foi elaborado. Trata-se de uma análise feita com base em um conjunto de dados contendo informações sobre os dados sociodemográficos, histórico do tabagismo, aspectos psicológicos e avaliação da qualidade de vida dos participantes de um Programa de Tratamento do Tabagismo, no período entre 2016 a 2020.


O estudo tinha como objetivo geral **traçar o perfil epidemiológico
de dependência nicotínica dos pacientes usuários de um certo Programa de Tratamento do Tabagismo**. Além disso, desejava-se: 

- observar os aspectos referentes ao consumo de tabaco;
- observar o grau de dependência à nicotina dos pacientes e 
- identificar a existência ou não de correlações entre algumas variáveis estudadas.

e responder as seguintes perguntas 

1. Qual a relação do perfil epidemiológico da população abordada com o seu grau de dependência à nicotina?
2. Quais as variáveis de exposição que se configurariam como possíveis fatores de risco para a dependência nicotínica na população atendida?

## Os dados 
Cada linha do conjunto de dados representa um participante do programa e cada coluna contém informações sobre os dados sociodemográficos, o histórico do tabagismo, os aspectos psicológicos e a qualidade de vida de cada participante, além do resultado do [teste de Fagerström](https://www.inca.gov.br/programa-nacional-de-controle-do-tabagismo/teste-fargestrom). O conjunto de dados inclui informações sobre: 


Teste de Fagerström Serve para mensurar o grau de dependência a nicotina;

- Dados sociodemográficos:

  - **Nome:** São apenas as iniciais para identificação do questionário;
  - **Idade:** Idade do paciente;
  - **Sexo:** Sexo do paciente (Feminino ou masculino);
  - **Estado Civil:** Estado civil de cada paciente (casado, solteiro, divorciado ou viúvo);
  - **Renda Familiar:** Renda familiar do paciente dividida em 3 categorias; 
  - **Escolaridade:** a escolaridade do paciente;
  
- Dados referentes ao Histórico do Tabagismo:

  - **Histórico Tabagista 4.1:** Com quantos anos começou a fumar;
  - **Quantidade diária de cigarros consumidos**;
  - **Histórico Tabagista 4.4:** Já tentei parar de fumar, mas não consegui;
  - **Histórico Tabagista 4.7:** número de vezes que Já tentei parar de fumar;

- Dados referentes aos aspectos psicológicos:

  - **Histórico Tabagista 4.5:** Já passei por algum constrangimento por causa do hábito de fumar;
  - **Histórico Tabagista 4.3:** Tenho medo de ter complicações sérias;
  - **Histórico Tabagista 4.6:** Acredito que tenho a capacidade de deixar de fumar;
  - **Histórico Tabagista 4.2:** Procuro esconder das pessoas que sou fumante;
  
- Dados referentes a qualidade de vida 

  - **EUROQOL 1:** Atividades habituais, como trabalho, estudos, atividades domésticas, atividades em família ou de lazer, entre outros;
  - **EUROQOL 2:** Dor/Mal-Estar;
  - **EUROQOL 3:** Ansiedade/Depressão;

 [^1]

[^1]: href="https://br.freepik.com/vetores/abstrato">Abstrato vetor criado por vectorjuice - br.freepik.com</a>

## Análise Inicial dos Dados 
Nesta etapa, vamos obter conhecimento a respeito de como os dados estão estruturados. Após importar o banco de dados usando o pacote `readxl`, vamos verificar se a base de dados precisa ser limpa. A função `dplyr::glimpse()` é útil para dar uma olhada na base. 

É possível perceber que algumas variáveis não foram classificadas corretamente, por exemplo, Estado civil é uma variável categórica, mas foi classificada como numérica. Além disso, as colunas precisam ser renomeadas. Assim, antes de começarmos a organizar a nossa base de dados, vamos listar quais problemas precisam ser solucionados. 

  1.	Algumas variáveis estão classificadas de forma errada;
  2.	Os nomes das variáveis precisam ser renomeados;
  3.	Classificar a idade em 5 categorias definidas previamente em reunião. 

Os códigos utilizados estão disponíveis [aqui](https://github.com/rodriguesbianca/perfil-epidemiologico)


Ao analisar os dados sobre a qualidade de vida, me deparei com um problema de visualização. Os dados possuíam 3 variáveis divididas em 3 categorias. As categorias referentes a Dor/Mal-Estar e Ansiedade/Depressão seguiam uma escala de "Nenhum" a "Extremo"", já as categorias sobre as atividades habituais seguiam a seguinte ordem:

1. Não tenho problemas em desempenhar as minhas atividades habituais;

2. Tenho apenas alguns problemas em desempenhar as minhas atividades habituais;

3. Sou incapaz de desempenhar as minhas atividades habituais.


A primeira coisa a se fazer ao se deparar com um desao de visualização é certifica-se de ter um sólido entendimento do contexto e do que é preciso comunicar.

Neste caso, o objetivo consistia em avaliar a qualidade de vida dos participantes de acordo com três aspectos, divididos em 3 categorias que especificavam uma escala. Então, com o intuito de resumir as informações para facilitar a comunicação e visualização dos dados, fiz algumas mudanças.

Primeiro, remodelamos a forma com que a variável "Atividades habituais" foi classificada. Ao fazer isso, fiz uma pequena modificação nas categorias, sem alterar o contexto. Nessa reedição, a variável ficou classificada da seguinte forma:

- Problemas em realizar atividades habituais:

  1. Não tenho problemas;
  
  2. Tenho problemas moderados;
  
  3. Tenho problemas extremos.

Também acrescentei a observação secundária: "Problemas extremos ao desempenhar as atividades habituais, significa que o participante é incapaz de desempenhar tais atividades". Por fim, escolhi um gráfico de barras horizontais para representar as informações.



Após deixar a base de dados da forma que queríamos, podemos prosseguir com a análise exploratória. (próximo post) 
