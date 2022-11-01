<h1 align="center">Issues encontradas<h1>

# O que são issues/bugs? 👨‍💻

Dentro da TI, uma issue é um espaço onde relatamos os bugs e defeitos encontrados dentro de uma aplicação na hora de rodar os testes. Além disso, dentro de uma issue, pode ser apontado um
ponto de melhoria para o software. 

---

## Issues encontradas durante a execução do projeto 🕵️

### Relacionadas a mensagens de retorno:

1. Quando enviamos uma requisição com e-mail inválido, recebemos a mensagem “email: email deve ser um email válido”, o que não está descrito na documentação, sendo algo muito sério a ser deixado de fora.

2. Mensagens: “email é obrigatório” e “password é obrigatório” em uma requisição sem body.

3. Quando enviamos uma requisição do tipo POST ou PUT com adm diferente de boolean, recebemos a mensagem “administrador: administrador deve ser ‘true’ ou ‘false’”

4.	Quando tentamos cadastrar ou editar usuário sem body recebemos a seguinte mensagem:

{

    “nome”: “nome é obrigatório”
	“email”: “email é obrigatório”
    “password”: “password é obrigatório”
    “administrador”: “administrador é obrigatório”
}

5. Quando enviamos uma requisição de um carrinho com produto duplicado, recebemos a mensagem, porém também é retornado o id do produto que está duplicado, muito útil, porém está em falta na documentação.

6. Quando enviamos uma requisição com um produto inexistente, retorna uma mensagem que parte dela não está na documentação.

7. Novamente, quando enviamos uma requisição com um produto que não possui quantidade suficiente no estoque, retorna uma mensagem que parte dela não está na documentação.

8. Se enviarmos qualquer requisição com body e com um JSON incorreto, é retornado a mensagem: “Adicione aspas em todos os valores. Para mais informações acesse a issue https://github.com/ServeRest/issues/225”, com um status code de 500


### Relacionadas ao status code:

1. Status code 401 com um email não cadastrado ou uma senha incorreta, devendo retornar um 400.

2. O status retornado com um json errado é de 500.


### **Lembrando que todos os testes foram realizados dentro dos limites da documentação da ServeRest, portanto, todos as issues reportatas são de retornos da API na qual a documentação não cobriu.**