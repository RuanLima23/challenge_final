<h1 align="center">Projeto ServeRest<h1>

# 💡O que é o projeto?

O objetivo desse projeto é testar, por meio da ferramento Postman, se a API pública ServeRest comporta todos os requisitos necessários para o bom funcionamento de um e-commerce. Esse desafio foi proposto pela empresa [Compass.UOL](https://compass.uol/pt/home/?utm_source=google-ads&utm_medium=ppc&utm_campaign=compasso-uol-institucional&utm_term=compass%20uol&gclid=CjwKCAjwwL6aBhBlEiwADycBINBMiBet_w1E1cMGIbyV_IypYiFmfwgwELtT3t0T0ywm-T7nxw58ORoCNssQAvD_BwE) para finalização do Programa de Bolsas iStudio QA. Esse README comporta alguns casos de teste que serão realizados na API e aborda algumas issues encontradas durante a construção dos testes. Vale ressaltar que além desses casos de testes, fluxos serão criados e validados além de outros testes menos relevantes.

---

# 🔬Casos de teste

O caso de teste é um conjunto de ações executadas para averiguar se um determinado recurso ou funcionalidade de software está funcionando corretamente. As validações serão feitas de acordo com a [documentação da ServeRest](https://serverest.dev). Segue os cenários propostos para os testes:



## CT1
CENÁRIO	➡️ Login do usuário

PRÉ-CONDIÇÕES ➡️ Usuário estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Ativar o body
3.	Informar o formato dos dados
4.	Inserir o e-mail
5.	Inserir a senha
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Login realizado com sucesso**

---

## CT2
CENÁRIO	➡️ Login sem dados

PRÉ-CONDIÇÕES ➡️ Usuário estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Ativar o body
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Dados são obrigatórios**

---

## CT3
CENÁRIO	➡️ Cadastrar usuário

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Ativar o body
3.	Informar o formato dos dados
4.  Inserir um nome 
5.	Inserir o e-mail
6.	Inserir senha
7.  Inserir adm
8.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT4
CENÁRIO	➡️ Cadastrar usuário sem dados

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Ativar o body
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Dados são obrigatórios**

---

## CT5
CENÁRIO	➡️ Cadastrar usuário com email já utilizado

PRÉ-CONDIÇÕES ➡️ E-mail já cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Ativar o body
3.	Informar o formato dos dados
4.  Inserir um nome 
5.	Inserir o e-mail
6.	Inserir senha
7.  Inserir adm
8.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Este e-mail já está sendo usado**

---

## CT6
CENÁRIO	➡️ Editar usuário

PRÉ-CONDIÇÕES ➡️ Usuário estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir o dado alterado
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro alterado com sucesso**

---

## CT7
CENÁRIO	➡️ Cadastrar usuário caso o ID não exista

PRÉ-CONDIÇÕES ➡️ ID inexistente

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir o dado alterado
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT8
CENÁRIO	➡️ Cadastrar produto

PRÉ-CONDIÇÕES ➡️ Usuário ter autorização

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Informar o ID
3.  Informar o token
4.  Ativar o body
5.	Informar o formato dos dados
6.  Inserir os dados
7.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT9
CENÁRIO	➡️ Cadastrar produto sem autorização

PRÉ-CONDIÇÕES ➡️ Usuário não tem autorização

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir os dados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente**

---
## CT10
CENÁRIO	➡️ Cadastrar produto sem dados

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Informar o ID
3.  Informar o token
4.  Ativar o body
5.	Informar o formato dos dados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Dados são obrigatórios**

---

## CT11
CENÁRIO	➡️ Editar produto

PRÉ-CONDIÇÕES ➡️ Produto estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Informar o token
4.  Ativar o body
5.	Informar o formato dos dados
6.  Inserir dados alterados
7.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT12
CENÁRIO	➡️ Cadastrar produto caso o ID não exista

PRÉ-CONDIÇÕES ➡️ ID inexistente

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Informar o token
4.  Ativar o body
5.	Informar o formato dos dados
6.  Inserir dados
7.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT13
CENÁRIO	➡️ Editar produto sem autorização

PRÉ-CONDIÇÕES ➡️ ID inexistente

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir dados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente**

---

## CT14
CENÁRIO	➡️ Cadastrar carrinho

PRÉ-CONDIÇÕES ➡️ Existir produtos cadastrados

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Informar token
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir produtos
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT15
CENÁRIO	➡️ Cadastrar carrinho mais de um carrinho 

PRÉ-CONDIÇÕES ➡️ Já existir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Informar token
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir produtos
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Não é permitido ter mais de 1 carrinho**

---

## CT16
CENÁRIO	➡️ Concluir compra

PRÉ-CONDIÇÕES ➡️ Já existir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.  Informar token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro excluído com sucesso**

---

## CT17
CENÁRIO	➡️ Cancelar compra e devolver produtos ao estoque

PRÉ-CONDIÇÕES ➡️ Já existir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.  Informar token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro excluído com sucesso. Estoque dos produtos reabastecido**

---

# ✅Execução do projeto

Dentro da ferramenta [Postman](https://www.postman.com), podemos criar e manipular nossos testes utilizando a linguagem JavaScript, junto 
com as bibliotecas [mocha](https://mochajs.org) e [chai](https://www.chaijs.com) e utilizando os conhecimentos 
desenvolvidos com o TDD. Com isso, temos infinitas possibilidades de testes que podem ser desenvolvidas. O 
Postman nos oferece alguns "Snippets" que são, basicamente, testes prontos, adaptados para testar APIs. O próprio Postman oferece um relatório de execução dos testes, podendo alterar o número de interações por collections ou pastas e até o intervalo de tempo (ms) entre a execução dos testes. Porém, para entregar um relatório bonito e elegante, será gerado um relatório em HTML utilizando o [Newman](https://www.npmjs.com/package/newman#html-reporter).

---

🖊️ Escrito por [Ruan Felipe de Lima](https://github.com/RuanLima23)