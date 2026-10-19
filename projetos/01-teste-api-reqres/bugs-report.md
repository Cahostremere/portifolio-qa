# Bugs encontrados - API ReqRes

## BUG-001 - Erro 404 vem sem nenhuma mensagem

Severidade: baixa
Prioridade: baixa
Endpoint: GET /api/users/23

Descrição:
Quando eu peço um usuário que não existe, a API devolve 404 mas o corpo vem vazio. Não chega a atrapalhar o uso, só que uma mensagem de erro ajudaria quem está consumindo a API a entender o que aconteceu.

Passos pra reproduzir:
1. Enviar GET pra https://reqres.in/api/users/23

Esperado: um JSON explicando o erro, tipo com código e mensagem.

Obtido: status 404 com o corpo vazio.

Status: registrado como observação (não é algo que trava o fluxo).
