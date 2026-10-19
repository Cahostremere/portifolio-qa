# Casos de teste - E-commerce fictício

## CT001 - Login com dados válidos
Prioridade: alta

Passos:
1. Abrir a tela de login
2. Preencher email e senha válidos
3. Clicar em Entrar

Esperado: o usuário entra e vai pra home.

---

## CT002 - Login com senha errada
Prioridade: alta

Passos:
1. Preencher uma senha incorreta
2. Clicar em Entrar

Esperado: mostrar mensagem de erro e não deixar entrar.

---

## CT003 - Login com os campos vazios
Prioridade: média

Esperado: a tela avisa que os campos são obrigatórios.

---

## CT004 - Adicionar produto ao carrinho
Prioridade: alta

Passos:
1. Escolher um produto
2. Clicar em Adicionar ao carrinho

Esperado: o produto aparece no carrinho com a quantidade certa.

---

## CT005 - Mudar a quantidade no carrinho
Prioridade: média

Passos:
1. Alterar a quantidade pra 2
2. Atualizar

Esperado: o total é recalculado.

---

## CT006 - Remover produto do carrinho
Prioridade: média

Esperado: o item sai e o carrinho se atualiza.

---

## CT007 - Aplicar um cupom inválido
Prioridade: baixa

Esperado: avisa que o cupom é inválido e não muda o valor.

---

## CT008 - Checkout com dados válidos
Prioridade: alta

Passos:
1. Preencher os dados pessoais e o endereço
2. Escolher a forma de pagamento
3. Finalizar a compra

Esperado: pedido confirmado com número gerado.

---

## CT009 - Checkout com campos obrigatórios vazios
Prioridade: alta

Esperado: a tela mostra os erros e não deixa finalizar.

---

## CT010 - Logout
Prioridade: média

Esperado: a sessão encerra e volta pra tela de login.
