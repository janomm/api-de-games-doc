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
Caso esta resposta aconteça, significa que ocorreu uma falha durante o processo da autenticação . Moticos: Token Inválido, Token expirado
