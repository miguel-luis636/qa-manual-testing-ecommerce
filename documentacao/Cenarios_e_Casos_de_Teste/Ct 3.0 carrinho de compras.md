# 3.0 Carrinho de Compras

**Módulo:** Carrinho de Compras

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Tipo de teste:** Manual funcional

**Ambiente:** Produção (site público)

---

## CT-025 — Adicionar produto ao carrinho

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página de um produto disponível em estoque |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a página de detalhes de um produto (PDP)
2. Selecionar um tamanho/variação válida
3. Clicar em "Adicionar ao carrinho" / "Comprar"

**Resultado esperado:**
O produto é adicionado ao carrinho com sucesso, o ícone/contador do carrinho é atualizado e o usuário recebe uma confirmação visual (modal, toast ou redirecionamento).

---

## CT-026 — Tentar adicionar produto sem selecionar variação obrigatória

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Produto exige seleção de tamanho/cor obrigatória |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a página de um produto que exige seleção de tamanho
2. Clicar em "Adicionar ao carrinho" sem selecionar o tamanho

**Resultado esperado:**
O sistema exibe uma mensagem solicitando a seleção da variação obrigatória e não adiciona o produto ao carrinho.

---

## CT-027 — Alterar quantidade de um item no carrinho

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Existe ao menos um produto no carrinho |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o carrinho
2. Alterar a quantidade de um item de 1 para 3 (usando o seletor de quantidade)

**Resultado esperado:**
O subtotal do item e o valor total do carrinho são recalculados corretamente, refletindo a nova quantidade.

---

## CT-028 — Remover item do carrinho

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Existe ao menos um produto no carrinho |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o carrinho
2. Clicar na opção "Remover" no item desejado

**Resultado esperado:**
O item é removido da lista imediatamente, e o valor total do carrinho é recalculado sem o item removido.

---

## CT-029 — Visualizar carrinho vazio

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Nenhum produto foi adicionado ao carrinho |
| **Prioridade** | Média |

**Passos:**
1. Acessar diretamente a página do carrinho sem ter adicionado produtos

**Resultado esperado:**
O sistema exibe uma mensagem informando que o carrinho está vazio, com um botão/link para continuar comprando.

---

## CT-030 — Aplicar cupom de desconto válido

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Existem produtos no carrinho e o testador possui um cupom válido (se disponível publicamente) |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o carrinho
2. Localizar o campo de cupom
3. Inserir um código de cupom válido
4. Clicar em "Aplicar"

**Resultado esperado:**
O desconto é aplicado e refletido no valor total, com uma confirmação visual de que o cupom foi aceito.

---

## CT-031 — Aplicar cupom inválido ou expirado

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Existem produtos no carrinho |
| **Prioridade** | Média |

**Passos:**
1. Acessar o carrinho
2. Inserir um código de cupom inválido/inexistente
3. Clicar em "Aplicar"

**Resultado esperado:**
O sistema exibe uma mensagem de erro clara, informando que o cupom é inválido, e o valor total permanece inalterado.

---

## CT-032 — Persistência do carrinho para usuário logado

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está logado e adicionou produtos ao carrinho |
| **Prioridade** | Média |

**Passos:**
1. Adicionar produtos ao carrinho estando logado
2. Fazer logout
3. Fazer login novamente com a mesma conta

**Resultado esperado:**
Os produtos adicionados anteriormente permanecem no carrinho após o novo login.

---

## CT-033 — Persistência do carrinho para usuário não logado (guest)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário não está logado |
| **Prioridade** | Baixa |

**Passos:**
1. Adicionar produtos ao carrinho sem estar logado
2. Fechar e reabrir o navegador (mesma sessão/cookies)
3. Acessar o site novamente

**Resultado esperado:**
Dependendo da política do site, o carrinho pode ou não persistir para usuários não logados. O comportamento observado deve ser documentado (não necessariamente um bug).

---

## CT-034 — Quantidade acima do estoque disponível

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Produto com estoque baixo/limitado identificado (ex: "últimas unidades") |
| **Prioridade** | Alta |

**Passos:**
1. Acessar um produto com estoque limitado
2. Tentar adicionar uma quantidade maior do que a disponível em estoque

**Resultado esperado:**
O sistema impede a adição da quantidade excedente ou exibe aviso informando a quantidade máxima disponível.

---

## CT-035 — Produto esgotado durante navegação no carrinho

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Produto no carrinho fica indisponível/esgotado (cenário de observação, difícil de forçar manualmente) |
| **Prioridade** | Baixa |

**Passos:**
1. Adicionar um produto ao carrinho
2. Verificar, em uma nova aba, se o mesmo produto/tamanho ainda está disponível
3. Caso identifique indisponibilidade, retornar ao carrinho e observar o comportamento

**Resultado esperado:**
O sistema deve sinalizar de alguma forma (aviso, remoção automática) que o item não está mais disponível, evitando avanço no checkout com produto indisponível.

---

## CT-036 — Resumo de valores no carrinho (subtotal, frete estimado, total)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Existem produtos no carrinho |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o carrinho com múltiplos produtos
2. Conferir os valores exibidos: subtotal, descontos (se houver) e total

**Resultado esperado:**
Os valores exibidos devem estar matematicamente corretos, somando corretamente o preço de cada item multiplicado pela quantidade.

---

## CT-037 — Continuar comprando a partir do carrinho

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página do carrinho |
| **Prioridade** | Baixa |

**Passos:**
1. Acessar o carrinho
2. Clicar em "Continuar comprando"

**Resultado esperado:**
O usuário é redirecionado para a página de listagem/produtos, mantendo os itens já adicionados ao carrinho.

---

## Observações Gerais

- Testes de cupom dependem da disponibilidade pública de códigos promocionais válidos; caso não haja nenhum disponível no momento, o cenário CT-030 pode ser registrado como "não testável no momento" em vez de reprovado
- Nenhuma etapa deste módulo avança até a finalização real da compra
- Recomenda-se testar o carrinho tanto para usuário logado quanto não logado (guest), quando essa opção existir no site
