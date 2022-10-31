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
CENÁRIO	➡️ Login com e-mail e/ou senha inválidos

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Ativar o body
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Email e/ou senha inválidos**

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
CENÁRIO	➡️ Cadastrar usuário com email indisponível

PRÉ-CONDIÇÕES ➡️ E-mail já estar cadastrado

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

## CT5
CENÁRIO	➡️ Buscar usuários

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Lista de usuários**

---

## CT6
CENÁRIO	➡️ Buscar usuário por ID

PRÉ-CONDIÇÕES ➡️ Usuário estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.  Informar o ID do usuário
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Usuário encontrado**

---

## CT7
CENÁRIO	➡️ Buscar usuário por ID inexistente

PRÉ-CONDIÇÕES ➡️ Usuário não estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.  Informar o ID do usuário
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Usuário não encontrado**

---

## CT8
CENÁRIO	➡️ Excluir usuário

PRÉ-CONDIÇÕES ➡️ Usuário estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do usuário
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro excluído com sucesso**

---

## CT9
CENÁRIO	➡️ Excluir usuário sem registro

PRÉ-CONDIÇÕES ➡️ Usuário não estar cadastrado ou já ter sido excluído

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do usuário
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Nenhum registro excluído**

---

## CT10
CENÁRIO	➡️ Excluir usuário com carrinho

PRÉ-CONDIÇÕES ➡️ Usuário possuir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do usuário
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Não é permitido excluir usuário com carrinho cadastrado**

---

## CT11
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

## CT12
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

## CT13
CENÁRIO	➡️ Alterar email do usuário para email indisponível

PRÉ-CONDIÇÕES ➡️ E-mail já estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Ativar o body
3.	Informar o formato dos dados
4.  Inserir um nome 
5.	Inserir o e-mail
6.	Inserir senha
7.  Inserir adm
8.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Este e-mail já está sendo usado**

---

## CT14
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

## CT15
CENÁRIO	➡️ Cadastrar produto com nome já utilizado

PRÉ-CONDIÇÕES ➡️ Nome indisponível

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Informar o ID
3.  Informar o token
4.  Ativar o body
5.	Informar o formato dos dados
6.  Inserir os dados
7.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Já existe produto com esse nome**

---

## CT16
CENÁRIO	➡️ Cadastrar produto sem autorização

PRÉ-CONDIÇÕES ➡️ Usuário não habilitar autorização

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir os dados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente, inválido, expirado ou usuário do token não existe mais**

---
    ## CT17
    CENÁRIO	➡️ Cadastrar produto com adm igual a false

    AÇÕES/PROCEDIMENTOS	➡️
    1.	Abrir uma requisição do tipo POST
    2.	Informar o ID
    3.  Ativar o body
    4.	Informar o formato dos dados
    5.  Inserir os dados
    6.	Enviar a requisição

    RESULTADO ESPERADO ➡️ **Rota exclusiva para administradores**

---

## CT18
CENÁRIO	➡️ Buscar produtos

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Lista de produtos**

---

## CT19
CENÁRIO	➡️ Buscar produto pelo ID

PRÉ-CONDIÇÕES ➡️ Produto estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.  Informar o ID do produto
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Produto encontrado**

---

## CT20
CENÁRIO	➡️ Buscar produto pelo ID inexistente

PRÉ-CONDIÇÕES ➡️ Produto não estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.  Informar o ID do produto
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Produto não encontrado**

---

## CT21
CENÁRIO	➡️ Excluir produto

PRÉ-CONDIÇÕES ➡️ Produto estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do produto
3.  Informar o token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro excluído com sucesso**

---

## CT22
CENÁRIO	➡️ Excluir produto sem registro

PRÉ-CONDIÇÕES ➡️ Produto não estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do produto
3.  Informar o token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Nenhum registro excluído**

---

## CT23
CENÁRIO	➡️ Excluir produto que está em um carrinho

PRÉ-CONDIÇÕES ➡️ Produto estar em um carrinho

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do produto
3.  Informar o token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Não é permitido excluir produto que faz parte de carrinho**

---

## CT24
CENÁRIO	➡️ Excluir produto sem token

PRÉ-CONDIÇÕES ➡️ Não ativar token

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar o ID do produto
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente, inválido, expirado ou usuário do token não existe mais**

---

## CT25
CENÁRIO	➡️ Excluir produto com adm igual a false

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.	Informar o ID
3.  Informar o token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Rota exclusiva para administradores**

---

## CT26
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

RESULTADO ESPERADO ➡️ **Registro alterado com sucesso**

---

## CT27
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

## CT28
CENÁRIO	➡️ Editar produto com nome já utilizado

PRÉ-CONDIÇÕES ➡️ Nome indisponível

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

## CT29
CENÁRIO	➡️ Editar produto sem autorização

PRÉ-CONDIÇÕES ➡️ Não informar o token

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir dados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente, inválido, expirado ou usuário do token não existe mais**

---

## CT30
CENÁRIO	➡️ Editar produto com adm igual a false

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo PUT
2.	Informar o ID
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir os dados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Rota exclusiva para administradores**

---

## CT31
CENÁRIO	➡️ Cadastrar carrinho

PRÉ-CONDIÇÕES ➡️ Produto estar cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Informar token
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir produtos
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Cadastro realizado com sucesso**

---

## CT32
CENÁRIO	➡️ Cadastrar carrinho com produto duplicado 

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Informar token
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir produtos duplicados
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Não é permitido possuir produto duplicado**

---

## CT33
CENÁRIO	➡️ Cadastrar mais de um carrinho 

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

## CT34
CENÁRIO	➡️ Cadastrar carrinho com produto inexistente

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Informar token
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir produtos 
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Produto não encontrado**

---

## CT35
CENÁRIO	➡️ Cadastrar carrinho com produto com estoque insuficiente

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Informar token
3.  Ativar o body
4.	Informar o formato dos dados
5.  Inserir produtos 
6.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Produto não possui quantidade suficiente**

---

## CT36
CENÁRIO	➡️ Cadastrar carrinho sem token

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo POST
2.  Ativar o body
3.	Informar o formato dos dados
4.  Inserir produtos 
5.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente, inválido, expirado ou usuário do token não existe mais**

---

## CT37
CENÁRIO	➡️ Buscar carrinhos

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Lista de carrinhos**

---

## CT38
CENÁRIO	➡️ Buscar carrinho por ID

PRÉ-CONDIÇÕES ➡️ Existir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Carrinho encontrado**

---

## CT39
CENÁRIO	➡️ Buscar carrinhos por ID inexistente

PRÉ-CONDIÇÕES ➡️ Não ter um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo GET
2.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Carrinho não encontrado**

---

## CT40
CENÁRIO	➡️ Finalizar compra

PRÉ-CONDIÇÕES ➡️ Existir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.  Informar token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro excluído com sucesso**

---

## CT41
CENÁRIO	➡️ Finalizar compra sem ter carrinho

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.  Informar token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Não foi encontrado carrinho para esse usuário**

---

## CT42
CENÁRIO	➡️ Finalizar compra sem token

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente, inválido, expirado ou usuário do token não existe mais**

---

## CT43
CENÁRIO	➡️ Cancelar compra e devolver produtos ao estoque

PRÉ-CONDIÇÕES ➡️ Existir um carrinho cadastrado

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.  Informar token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Registro excluído com sucesso. Estoque dos produtos reabastecido**

---

## CT44
CENÁRIO	➡️ Cancelar compra sem ter carrinho

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.  Informar token
4.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Não foi encontrado carrinho para esse usuário**

---

## CT45
CENÁRIO	➡️ Cancelar compra sem token

AÇÕES/PROCEDIMENTOS	➡️
1.	Abrir uma requisição do tipo DELETE
2.  Informar qual o tipo de exclusão do carrinho (concluir/cancelar)
3.	Enviar a requisição

RESULTADO ESPERADO ➡️ **Token de acesso ausente, inválido, expirado ou usuário do token não existe mais**

---

# ✅Execução do projeto

Dentro da ferramenta [Postman](https://www.postman.com), podemos criar e manipular nossos testes utilizando a linguagem JavaScript, junto 
com as bibliotecas [mocha](https://mochajs.org) e [chai](https://www.chaijs.com) e utilizando os conhecimentos 
desenvolvidos com o TDD. Com isso, temos infinitas possibilidades de testes que podem ser desenvolvidas. O 
Postman nos oferece alguns "Snippets" que são, basicamente, testes prontos, adaptados para testar APIs. O próprio Postman oferece um relatório de execução dos testes, podendo alterar o número de interações por collections ou pastas e até o intervalo de tempo (ms) entre a execução dos testes. Porém, para entregar um relatório bonito e elegante, será gerado um relatório em HTML utilizando o [Newman](https://www.npmjs.com/package/newman#html-reporter).

---

🖊️ Escrito por [Ruan Felipe de Lima](https://github.com/RuanLima23)