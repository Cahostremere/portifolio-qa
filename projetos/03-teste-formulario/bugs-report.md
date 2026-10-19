# Bugs encontrados - Formulário web

## BUG-001 - Formulário aceita e-mail sem domínio

Severidade: média
Prioridade: alta
Onde: campo de e-mail

Passos pra reproduzir:
1. Preencher o e-mail com "teste@"
2. Enviar o formulário

Esperado: recusar e avisar que o e-mail está inválido.
Obtido: o formulário aceita e envia normalmente.

Status: aberto.
