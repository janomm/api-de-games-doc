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
##### Falha na autenticação! 401
Caso esta resposta aconteça, significa que ocorreu uma falha durante o processo da autenticação . Moticos: Token Inválido, Token expirado
