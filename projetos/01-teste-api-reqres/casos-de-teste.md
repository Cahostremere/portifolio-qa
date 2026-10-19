# Casos de teste - API ReqRes

Usei a API pública ReqRes pra treinar teste de API. Anotei abaixo os casos que rodei, com os passos e o que eu esperava em cada um.

## CT001 - Listar usuários

Prioridade: alta
Endpoint: GET /api/users?page=2

Passos:
1. Enviar GET pra https://reqres.in/api/users?page=2

O que eu esperava:
- Status 200
- Corpo com a lista de usuários
- Campos de paginação: page, per_page, total e total_pages
- Cada usuário com id, email, first_name, last_name e avatar

Resultado: veio 200 e os dados estavam certos.

---

## CT002 - Buscar usuário por ID

Prioridade: alta
Endpoint: GET /api/users/2

Passos:
1. Enviar GET pra https://reqres.in/api/users/2

O que eu esperava:
- Status 200
- Dados do usuário com id 2

Resultado: veio 200 com os dados do usuário 2.

---

## CT003 - Buscar usuário que não existe

Prioridade: média
Endpoint: GET /api/users/23

Passos:
1. Enviar GET pra https://reqres.in/api/users/23

O que eu esperava:
- Status 404
- Nenhum dado no corpo

Resultado: veio 404 com o corpo vazio.

---

## CT004 - Criar usuário

Prioridade: alta
Endpoint: POST /api/users

Corpo enviado:
```json
{
  "name": "Teste QA",
  "job": "Analista de Testes"
}
```

Passos:
1. Enviar POST com o corpo acima

O que eu esperava:
- Status 201
- Retorno com id, name, job e createdAt

Resultado: veio 201 com id gerado e createdAt.

---

## CT005 - Atualizar usuário (PUT)

Prioridade: alta
Endpoint: PUT /api/users/2

Corpo enviado:
```json
{
  "name": "Teste QA Atualizado",
  "job": "QA Senior"
}
```

Passos:
1. Enviar PUT com o corpo acima

O que eu esperava:
- Status 200
- Retorno com name, job e updatedAt

Resultado: veio 200 com os dados atualizados.

---

## CT006 - Atualizar usuário (PATCH)

Prioridade: média
Endpoint: PATCH /api/users/2

Corpo enviado:
```json
{
  "job": "QA Pleno"
}
```

Passos:
1. Enviar PATCH com o corpo acima

O que eu esperava:
- Status 200
- Retorno só com o campo alterado e o updatedAt

Resultado: veio 200 com o job e o updatedAt.

---

## CT007 - Excluir usuário

Prioridade: alta
Endpoint: DELETE /api/users/2

Passos:
1. Enviar DELETE pra https://reqres.in/api/users/2

O que eu esperava:
- Status 204
- Corpo vazio

Resultado: veio 204 sem corpo.
