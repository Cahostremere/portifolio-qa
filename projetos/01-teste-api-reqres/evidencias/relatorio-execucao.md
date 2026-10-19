# Relatório de execução - Testes de API (ReqRes)

Data: 18/10/2026
Ambiente: API pública da ReqRes
Base: https://reqres.in/api

Rodei os 7 casos de teste. Todos passaram.

## Resultado de cada caso

| ID | Caso | Esperado | Obtido | Resultado |
|----|------|----------|--------|-----------|
| CT001 | Listar usuários | 200 | 200 | passou |
| CT002 | Buscar usuário por ID | 200 | 200 | passou |
| CT003 | Buscar ID inexistente | 404 | 404 | passou |
| CT004 | Criar usuário | 201 | 201 | passou |
| CT005 | Atualizar usuário (PUT) | 200 | 200 | passou |
| CT006 | Atualizar usuário (PATCH) | 200 | 200 | passou |
| CT007 | Excluir usuário | 204 | 204 | passou |

## Detalhes

### CT001 - Listar usuários

Requisição: GET https://reqres.in/api/users?page=2
Status: 200

Corpo (resumido):
```json
{
  "page": 2,
  "per_page": 6,
  "total": 12,
  "total_pages": 2,
  "data": [
    {
      "id": 7,
      "email": "michael.lawson@reqres.in",
      "first_name": "Michael",
      "last_name": "Lawson",
      "avatar": "https://reqres.in/img/faces/7-image.jpg"
    },
    {
      "id": 8,
      "email": "lindsay.ferguson@reqres.in",
      "first_name": "Lindsay",
      "last_name": "Ferguson",
      "avatar": "https://reqres.in/img/faces/8-image.jpg"
    }
  ]
}
```

Conferi: status 200, campos de paginação presentes, lista com os usuários e os campos id, email, first_name, last_name e avatar em cada um.

### CT002 - Buscar usuário por ID

Requisição: GET https://reqres.in/api/users/2
Status: 200

Corpo:
```json
{
  "data": {
    "id": 2,
    "email": "janet.weaver@reqres.in",
    "first_name": "Janet",
    "last_name": "Weaver",
    "avatar": "https://reqres.in/img/faces/2-image.jpg"
  }
}
```

Conferi: status 200, id igual ao que eu pedi (2) e os dados do usuário certos.

### CT003 - Buscar usuário inexistente

Requisição: GET https://reqres.in/api/users/23
Status: 404

O corpo veio vazio.

Conferi: status 404 e nenhum dado retornado.

Obs: o corpo vazio é o que eu registrei no bugs-report.md. Não quebra nada, mas uma mensagem de erro seria melhor.

### CT004 - Criar usuário

Requisição: POST https://reqres.in/api/users
Corpo enviado:
```json
{
  "name": "Teste QA",
  "job": "Analista de Testes"
}
```
Status: 201

Corpo:
```json
{
  "name": "Teste QA",
  "job": "Analista de Testes",
  "id": "433",
  "createdAt": "2026-10-18T23:52:29.730Z"
}
```

Conferi: status 201, id gerado, createdAt presente e os dados que enviei refletidos na resposta.

### CT005 - Atualizar usuário (PUT)

Requisição: PUT https://reqres.in/api/users/2
Corpo enviado:
```json
{
  "name": "Teste QA Atualizado",
  "job": "QA Senior"
}
```
Status: 200

Corpo:
```json
{
  "name": "Teste QA Atualizado",
  "job": "QA Senior",
  "updatedAt": "2026-10-18T23:52:30.006Z"
}
```

Conferi: status 200, dados atualizados e updatedAt presente.

### CT006 - Atualizar usuário (PATCH)

Requisição: PATCH https://reqres.in/api/users/2
Corpo enviado:
```json
{
  "job": "QA Pleno"
}
```
Status: 200

Corpo:
```json
{
  "job": "QA Pleno",
  "updatedAt": "2026-10-18T23:52:30.281Z"
}
```

Conferi: status 200, só o campo enviado retornado e updatedAt presente.

### CT007 - Excluir usuário

Requisição: DELETE https://reqres.in/api/users/2
Status: 204

Corpo vazio.

Conferi: status 204 e corpo vazio.

## Fechamento

Os 7 casos passaram e a API atendeu o que eu esperava. O único ponto que anotei foi o corpo vazio no 404, que ficou registrado como BUG-001.
