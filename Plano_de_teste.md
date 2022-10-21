<h1 align="center">Plano de Teste - Funcionalidade da API ServeRest<h1>


#### Autor: [Ruan Felipe de Lima](https://github.com/RuanLima23)

#### Programa de Bolsas iStudio QA

#### Empresa: [Compass.UOL](https://compass.uol/pt/home/?utm_source=google-ads&utm_medium=ppc&utm_campaign=compasso-uol-institucional&utm_term=compass%20uol&gclid=CjwKCAjwwL6aBhBlEiwADycBIMDfXVuLSCkD0bVpoOEgljwWix7wNBauO6GBWMvYmJ_3L_chrPHlQRoC_jIQAvD_BwE)

---

## Sumário

1.	[INTRODUÇÃO](#introdução)

2.	[PESSOAS ENVOLVIDAS](#pessoas-envolvidas)

3.	[FUNCIONALIDADES A SEREM TESTADAS](#funcionalidades-a-serem-testados)

4.	[LOCAL DOS TESTES](#local-dos-testes)

5.	[RECURSOS NECESSÁRIOS](#recursos-necessários)

6.	[RISCOS](#riscos)

7.	[COMO O RESULTADO DOS TESTES SERÁ DIVULGADO](#como-os-resultados-do-teste-será-divulgado)

8.	[CRONOGRAMA](#cronograma)

---

## Introdução
O projeto tem como principal objetivo validar se a API corresponde aos requisitos mínimos propostos para o funcionamento dentro um ambiente de produção. Os testes que serão realizados têm o intuito de validar se a ServeRest atende a premissa de um e-commerce. Dentro deste documento de teste, compõe os seguintes desafios:

•	Identificar as funcionalidades que serão testadas;

•	Identificar o que será necessário para realizar e executar os testes;

---

## Pessoas envolvidas
Por ser um projeto desenvolvido individualmente para o Programa de Bolsas iStudio QA, apenas eu o desenvolverei. A contribuição de outros colegas e amigos estarão referenciados no tópico “Referências e agradecimentos” dentro do README.

---

## Funcionalidades a serem testados
Como mencionado anteriormente, os testar estão voltados para os principais objetivos e funcionalidades da API. Pensando em um e-commerce, precisamos validar se a API atenderá as funcionalidades a fim de que o usuário possa finalizar suas compras de forma simples e sem problemas. Sendo mais específico, será realizado testes unitários e regressivos para validar as rotas login, usuários, produtos e carrinhos disponibilizadas na documentação e seus responses status code, body responses e mensagens, além de validar se algumas estruturas de dados correspondem ao que foi inserido e retornado. Vale lembrar que esses testes abrangem uma série de requisitos não funcionais a serem testados simultaneamente, como usabilidade e segurança.

---

## Local dos testes
A ServeRest é uma API pública na qual seu objetivo é voltado ao aprendizado de novos QAs. Ela pode ser chamada em dois tipos de ambiente, local e web. Os testes serão realizados em um ambiente local disponibilizado pela própria API. As validações serão feitas nesse ambiente pensando nos possíveis conflito com o ambiente de produção, simulando assim um ambiente real.

---

## Recursos necessários
Os recursos necessários para a realização desses testes são alguns softwares e conhecimentos vistos dentro do programa de bolsas:

•	Node js;

•	Postman com Newman, para execução e criação dos testes;

•	Conhecimento em Javascript para a realização dos testes;

•	Xmind, para criação de um mapa mental da API;

•	VS code;

•	Conhecimento em versionamento de código com GIT e GitHub para armazenamento dos scrips e dos documentos.

---

## Riscos
Os potenciais riscos na hora do teste são:

•	A falta de internet para a execução dos testes, o que pode ser facilmente resolvida garantindo mais de um tipo de conexão. 

•	A sobrecarga de execuções sendo realizadas ao mesmo sem um delay, pode potencialmente falhar alguns testes, por mais que esteja em um ambiente local. 

---

## Como os resultados do teste será divulgado	
Será gerado um documento HTML utilizando o newman a partir da linha de comando. O próprio postman nos gera um relatório dos testes. Caso algum defeito seja encontrado, ele será documentado.

---

## Cronograma
Esse projeto tem como data de início 18/10/2022 e tem como fim dia 31/10/2022.
Tenho como objetivo concluir todas as atividades necessárias para a elaboração dos testes nesse período.



