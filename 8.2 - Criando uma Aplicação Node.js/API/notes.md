# Método de requisições HTTP
## 1.Get
- Leitura
Exemplo
```js
    const express = require('express');

const app = express();

app.get("/message", (request, response) => {
    response.send("Hello, World!")
})

const PORT = 3333;
app.listen(PORT, () => console.log(`Server is running on Port ${PORT}`));
```
### 1.1 Route Params
São rotas que retornam obrigatoriamente parâmetros simples conforme a solicitação do user. Sua criação se dá acrescentando '/:' (dois pontos no endereço). Exemplo:

```js
    app.get("/message/:id/:user", (request, response) => {
    response.send("Hello, World!")
    )}
```
Neste caso, acrescentei dois parâmetros: Id e User.

### 1.2 Query Params
São parâmetros não orbigatórios, ou seja, a página do endereço é excutada com eles ou não. Para criá-los, deve-se incluir no endereço o seguinte (tudo junto):
    - endereço.com.br
    - /recurso
    - ? (separador recurso-chave)
    - chave
    - =valor
    - & (separador chave-chave)

## 2.Post
- Criação
## 3.Put
- Atualização
## 4.Delete
- Deletar
## 5.Patch
- Atualização Parcial

# 5 metodos do controller (boa pratica)
    * index - GET para listar vários registros.
    * show - GET para exibir um registro especifico.
    * create - POST para criar um registro.
    * update - PUT para atualizar um registro
    * delete - DELETE para remover um registro.