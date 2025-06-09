# AllBooks

Boas vindas a API do AllBooks - DEV branch!

O AllBooks é uma loja virtual que vende livros da Casa do Código. 
É um MVP que tá só começando e ainda tem muitas funcionalidades novas para serem desenvolvidas.

# JSONServer + JWT Auth

Essa é uma API Rest mockada, utilizando json-server e JWT.

## 🛠️ Instalação 🛠️

```bash
$ npm install
$ npm run start-auth
```
## 🛠️ Como se registrar? 🛠️

Você pode fazer isso efetuando uma requisição post para:

```
POST http://localhost:8000/public/registrar
```

Com os seguintes dados:

```
{
    "nome": "rodrigo lobo",
    "email": "rodrigo@alura.com.br",
    "senha": "123456",
    "endereco": "Rua 8, Lote 1",
    "complemento": "Parque Esplanada II",
    "cep": "04101-300"
}
```

Repare que o e-mail é um campo único e usuários com e-mails duplicados não serão persistidos.

## 🛠️ Como fazer login? 🛠️

Você pode fazer isso efetuando uma requisição post para:

```
POST http://localhost:8000/public/login
```

Com os seguintes dados:


```
{
  "email": "rodrigo@alura.com.br",
  "senha":"123456"
}
```

Você vai receber um token no seguinte formato:

```
{
   "access_token": "<ACCESS_TOKEN>",
   "user": { ... dados do usuário ... }
}
```

## Autenticar próximas requests?

E então, adicionar este mesmo token ao header das próximas requisições:

```
Authorization: Bearer <ACCESS_TOKEN>
```
