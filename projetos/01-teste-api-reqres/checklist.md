# Checklist - Testes de API (ReqRes)

## Antes de começar
- [ ] Importei a coleção `postman-collection.json`
- [ ] Base da API confirmada: https://reqres.in/api

## Fluxo principal
- [ ] GET /api/users?page=2 responde 200
- [ ] GET /api/users/2 responde 200
- [ ] POST /api/users responde 201
- [ ] PUT /api/users/2 responde 200
- [ ] DELETE /api/users/2 responde 204

## Validação da resposta
- [ ] O corpo vem no formato esperado
- [ ] Os campos obrigatórios estão presentes
- [ ] Os tipos de dados batem
- [ ] A paginação funciona com valores diferentes de page

## Cenários negativos
- [ ] GET /api/users/23 responde 404
- [ ] Endpoint inexistente devolve erro em vez de quebrar
