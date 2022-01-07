---
date: "2021-01-01"
draft: false
excerpt: "Existe relação entre o perfil epidemiológico da população abordada com o seu grau de dependência à nicotina?"
subtitle: ""
title: Perfil epidemiológico de dependência nicotínica - Parte II
weight: 3
tags:
  - analise de dados
categories:
  - estágio supervisionado
  - visualização de dados
---

## Introdução

Olá!

Esse post faz parte de uma série de posts, que tem como objetivo documentar algumas das minhas atividades desenvolvidas durante a realização do estágio supervisionado, que foi realizado no Laboratório de Análises Estatísticas - LANEST, localizado na Universidade Federal de Campina Grande (UFCG). 

Esse é o segundo post, então caso não tenha lido o post anterior, acesse esse link! 

--- 

A manipulação de dados, bem como as análises e visualizações foram realizadas
no *Software R*, também utilizei o *Microsoft Excel* e *Adobe Illustrator* para auxiliar na criação de alguns gráficos. Como todas as variáveis eram categóricas, para a visualização de informações foram utilizados tabelas e gráficos de barras. Os códigos estão disponíveis no meu Github ([clique aqui](https://github.com/rodriguesbianca/perfil-epidemiologico)).

## Análise de dados 
No Programa de Tratamento do Tabagismo, entre os anos de 2016 a 2020, 70,1% dos pacientes eram do sexo feminino, enquanto 29,9% eram do sexo masculino. 

Com relação à idade, 32,8% dos pacientes tinham entre 40 e 49 anos. Além disso, pela Figura 1, vemos que aproximadamente, 31,3% tinham idades entre 50 e 59 anos, aqueles com 60 anos ou mais corresponderam a 20,9% do total e 13, 4% apresentaram idades entre 30 e 39 anos e apenas 1,5% tinham entre 18 e 29 anos. 



<div align="center">
  <img src="Idade_tabagismo.png"/>  
  
  *Figura 1: Gráfico de barras relativo ao Percentual dos participantes de acordo com a idade.*
</div>



A Tabela abaixo contém os dados referentes ao nível de escolaridade, em que 28, 4%
dos participantes declararam ter apenas o ensino fundamental incompleto, enquanto
17, 9% disseram ter o ensino fundamental completo. Sobre o ensino médio, 25, 4% disseram ter o ensino médio completo, e 4, 5% incompleto. Já quanto ao nível superior, 20, 9% disseram ter ensino superior completo e 1, 5% o ensino superior incompleto. Apenas uma pessoa optou por não responder.


| Escolaridade                  | Total | Percentual |
|-------------------------------|:-----:|:----------:|
| Ensino fundamental incompleto |   19  |   28, 4%   |
| Ensino fundamental completo   |   12  |   17, 9%   |
| Ensino médio incompleto       |   3   |    4, 5%   |
| Ensino médio completo         |   17  |   25, 4%   |
| Ensino superior incompleto    |   1   |    1, 5%   |
| Ensino superior completo      |   14  |   20, 9%   |


No que diz respeito à renda familiar, 1% dos entrevistados não responderam e, pelo gráfico apresentado na Figura 2, podemos ver que a renda familiar mensal da maior parte dos entrevistados, isto é, 55%, é menor ou igual a um salário mínimo, 30% entre dois e três salários mínimos e 15% declararam ter uma renda superior a três salários mínimos.

<div align="center">
  <img src="renda.png"/>  
  
  *Figura 2: Gráfico de barras baseado nas respostas sobre a renda familiar.*
</div>


Quanto ao estado civil, 43,3% dos participantes do programa eram casadas(os) ou vivem com companheiros(as). De acordo com o gráfico apresentado na Figura (3), 31,3% afirmaram ser solteiros(as), enquanto 14,9% eram divorciados(as) ou separados(as) e 10,4% declararam ser viúvos(as).

<div align="center">
  <img src="estado-civil.png"/>  
  
  *Figura 3: Gráfico de barras baseado nas respostas sobre o Estado civil.*
</div>


Quando questionados sobre a idade em que começaram a fumar, as respostas variaram entre 9 e 41 anos. Em média, os entrevistados começaram a fumar aos 16 anos. 
Para a realização deste estudo foi proposta a categorização das idades em três (3) faixas etárias. São elas:

- **Criança:** a pessoa com até doze anos de idade incompletos;
- **Adolescente:** aquela com idade entre doze e dezoito anos;
- **Adultos:** a pessoa com idade a partir de dezoito anos.

Assim, pela Figura (4) vemos que 55% dos entrevistados começaram a fumar
durante a adolescência e 7% começaram a fumar ainda crianças.

<div align="center">
  <img src="comecou-fumar.png"/>  
  
  *Figura 4: Gráfco de barras baseado nas respostas sobre a idade em que os pacientes começaram a fumar.*
</div>


Em relação à quantidade de cigarros consumidos diariamente, a maioria dos participantes do programa consomem entre 11 a 20 cigarros, correspondendo a um total de 56, 7% dos entrevistados. Pelo gráfico apresentado na Figura (5), vemos que 17, 9% utilizam entre 21 e 30 cigarros.  


Levando em consideração que o acondicionamento de cigarros destinados à comercialização geralmente é feito em maço ou carteira de 20 cigarros cada, isto implica dizer que, ao somar o percentual de participantes que fazem uso de mais de 31 cigarros por dia, **28, 3% dos participantes do programa consomem mais de uma carteira de cigarros diariamente**.

<div align="center">
  <img src="cigarros-diarios.png"/>  
  
  *Figura 5: Gráfco de barras baseado nas respostas sobre a quantidade de cigarros consumidos diariamente.*
</div>

Sobre a quantidade de vezes em que os participantes do programa tentaram parar
de fumar, 79,1% afirmaram já tentar parar de fumar, mas não conseguiram. 31, 4%
deles também disseram ter tentado parar de fumar ao menos 3 vezes, 25% disseram que tentaram apenas uma vez e 20, 9% afirmaram que não tentaram parar de fumar nenhuma vez.


<div align="center">
  <img src="paroudefumar.png"/>  
  
  *Figura 6: Gráfco de barras baseado nas respostas sobre a quantidade de cigarros consumidos diariamente.*
</div>

Entre os participantes do programa que responderam às perguntas acerca dos aspectos psicológicos, pelo Gráfico da Figura (7), podemos ver que, aproximadamente 34,30% dos participantes procuram esconder das pessoas que é fumante. 96,92% acredita ter a capacidade de parar de fumar, enquanto 88, 10% diz ter medo de ter complicações sérias, e 62,12% alegam ter passado por algum constrangimento por causa do hábito de fumar.


<div align="center">
  <img src="HT.png"/>  
  
  *Figura 7: Gráfico de barras baseado nas respostas dos participantes em relação ao seu aspecto psicológico.*
</div>


A Figura (8) resume as informações sobre a qualidade de vida dos participantes
do Programa. No que se refere às atividades habituais (como trabalho, estudos, atividades domésticas, atividades em família ou de lazer, entre outros), foi questionado aos participantes se eles possuíam algum problema em desempenhar tais atividades em decorrência ao uso do cigarro. Os resultados mostraram que 65,7% não tem problemas em realizar essas atividades, 25,4% diz ter problemas em desempenhá-las, enquanto 9% é incapaz de desempenhar as suas atividades habituais.

<div align="center">
  <img src="qualidade_vida.jpg"/>  
  
  *Figura 8: Gráfico de barras baseado nas respostas dos participantes em relação à avaliação sobre a qualidade de vida.*
</div>
