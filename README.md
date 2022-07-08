# API de Games
Esta api é utilizada para consumir o rest do meu projeto

## Endpints
### GET/games
Este endpoint é responsável por retornar todos os games do banco de dados
#### Parâmetros
Nenhum
#### Respostas
##### OK! 200
Caso esta resposta aconteça, você vai receber a listagem de todos os games.
Exemplode resposta:
```
{
    "id": 1,
    "title": "Mario Kart",
    "year": 1992,
    "price": 8,
    "createdAt": "2022-07-07T18:11:54.000Z",
    "updatedAt": "2022-07-07T18:59:10.000Z"
}
```
##### Falha na autenticação! 401
Caso esta resposta aconteça, significa que ocorreu uma falha durante o processo da autenticação . Motivos: Token Inválido, Token expirado.
Exemplo de resposta:
```
{
    "err": "Token Inválido"
}
```

### POST /auth
Este endpoint é responsável por fazer o processo de login
#### Parâmetros
email: E-mail do usuário cadastrado no sistema.
password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail.
Exemplo de parâmetro:
```
{
    "email": "joao@games.com",
    "password": "Teste123"
}
```

#### Respostas
##### OK! 200
Caso esta resposta aconteça, você vai receber o token JWT para acessar endpoints protegistos da API.
Exemplode resposta:
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJqYW5vbW1AZ21haWwuY29tIiwiaWF0IjoxNjU3MjkxOTUzLCJleHAiOjE2NTc0NjQ3NTN9.0eLbVtgHcDs6UrOana4nK64xsplnYxJVGTp3v7_1uQg"
}
```
##### Falha na autenticação! 401
Caso esta resposta aconteça, significa que ocorreu uma falha durante o processo da autenticação . Motivos: Senha ou e-mail incorreto.
Exemplo de resposta:
```
{
    "err": "Credenciais inválidas!"
}
```
