# Casos de teste - Formulário web

## CT001 - Enviar o formulário com os dados certos
Prioridade: alta

Passos:
1. Preencher todos os campos válidos
2. Clicar em Enviar

Esperado: mostra a confirmação de sucesso.

---

## CT002 - Enviar com os campos obrigatórios vazios
Prioridade: alta

Esperado: a tela aponta os campos que faltam.

---

## CT003 - E-mail inválido
Prioridade: alta

Exemplos que testei: teste@, @teste.com, teste.com

Esperado: recusa e avisa que o formato está errado.

---

## CT004 - E-mail válido
Prioridade: alta

Exemplo: teste@exemplo.com

Esperado: aceita sem reclamar.

---

## CT005 - Texto com caractere especial
Prioridade: média

Esperado: aceita só o que faz sentido pro campo e ignora o resto.

---

## CT006 - Passar do limite de caracteres
Prioridade: média

Esperado: corta no limite do campo.

---

## CT007 - Clicar duas vezes em enviar
Prioridade: média

Passos:
1. Clicar em Enviar duas vezes rápido

Esperado: não envia o mesmo cadastro duas vezes.

---

## CT008 - Campo que só aceita número
Prioridade: média

Esperado: aceita apenas números quando é o caso.
