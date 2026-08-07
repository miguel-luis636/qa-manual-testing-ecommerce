# 4.0 Checkout (sem conclusão de compra)

**Módulo:** Checkout

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Tipo de teste:** Manual funcional

**Ambiente:** Produção (site público)

> ⚠️ Nenhum caso de teste deste módulo avança até a confirmação/finalização real do pedido. Nenhum dado de pagamento real (cartão, etc.) é inserido em nenhuma etapa.

---

## CT-038 — Iniciar checkout com carrinho preenchido

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Existe ao menos um produto no carrinho |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o carrinho com produtos adicionados
2. Clicar em "Finalizar compra" / "Fechar pedido"

**Resultado esperado:**
O usuário é direcionado para a próxima etapa do checkout (identificação/login, caso ainda não esteja logado, ou diretamente para endereço de entrega).

---

## CT-039 — Checkout exige login ou identificação

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário não está logado e possui produtos no carrinho |
| **Prioridade** | Alta |

**Passos:**
1. Com o carrinho preenchido, iniciar o checkout sem estar logado

**Resultado esperado:**
O sistema solicita login ou oferece opção de continuar como convidado (se disponível), antes de prosseguir para as etapas seguintes.

---

## CT-040 — Seleção de endereço de entrega já cadastrado

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário logado possui mais de um endereço cadastrado |
| **Prioridade** | Alta |

**Passos:**
1. Avançar no checkout até a etapa de entrega
2. Selecionar um endereço diferente do padrão exibido

**Resultado esperado:**
O endereço selecionado é aplicado corretamente ao pedido, e o frete/prazo é recalculado conforme o novo endereço.

---

## CT-041 — Cadastro de novo endereço durante o checkout

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na etapa de entrega do checkout |
| **Prioridade** | Média |

**Passos:**
1. Na etapa de entrega, selecionar "Adicionar novo endereço"
2. Preencher os campos obrigatórios com dados fictícios válidos (CEP, rua, número, bairro, cidade)
3. Salvar o endereço

**Resultado esperado:**
O novo endereço é salvo com sucesso e fica selecionado como endereço de entrega para o pedido atual.

---

## CT-042 — Cálculo de frete durante o checkout

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Endereço de entrega definido |
| **Prioridade** | Alta |

**Passos:**
1. Avançar até a etapa onde o frete é exibido
2. Conferir se as opções de frete (valor e prazo) estão sendo exibidas corretamente

**Resultado esperado:**
As opções de frete disponíveis são exibidas com valor e prazo de entrega, condizentes com o endereço selecionado.

---

## CT-043 — Seleção entre diferentes opções de frete

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Mais de uma opção de frete está disponível (ex: padrão e expresso) |
| **Prioridade** | Média |

**Passos:**
1. Na etapa de entrega, selecionar uma opção de frete diferente da padrão
2. Observar o valor total do pedido

**Resultado esperado:**
O valor total do pedido é atualizado corretamente ao trocar a opção de frete selecionada.

---

## CT-044 — Visualizar resumo do pedido antes do pagamento

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Etapa de entrega concluída |
| **Prioridade** | Alta |

**Passos:**
1. Avançar para a etapa de pagamento
2. Conferir o resumo do pedido exibido (itens, quantidades, subtotal, frete, total)

**Resultado esperado:**
Os valores exibidos no resumo devem ser idênticos aos valores apresentados anteriormente no carrinho, sem divergências.

---

## CT-045 — Seleção da forma de pagamento (sem finalizar)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na etapa de pagamento |
| **Prioridade** | Alta |

**Passos:**
1. Na etapa de pagamento, selecionar a opção "Cartão de crédito"
2. Observar os campos exibidos

**Resultado esperado:**
Os campos correspondentes ao cartão de crédito (número, validade, CVV, nome impresso) são exibidos corretamente. **O teste é interrompido neste ponto — nenhum dado real é inserido.**

---

## CT-046 — Alternar entre formas de pagamento disponíveis

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na etapa de pagamento com múltiplas opções disponíveis (cartão, boleto, Pix) |
| **Prioridade** | Média |

**Passos:**
1. Selecionar "Cartão de crédito" e observar os campos
2. Alternar para "Boleto" e observar os campos
3. Alternar para "Pix" (se disponível) e observar os campos

**Resultado esperado:**
Os campos exibidos mudam corretamente de acordo com a forma de pagamento selecionada, sem sobreposição de informações da opção anterior.

---

## CT-047 — Voltar etapa no checkout sem perder dados preenchidos

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário avançou da etapa de entrega para a etapa de pagamento |
| **Prioridade** | Média |

**Passos:**
1. Preencher a etapa de entrega e avançar para pagamento
2. Clicar em "Voltar" para revisar a etapa de entrega

**Resultado esperado:**
Os dados preenchidos anteriormente (endereço, frete selecionado) permanecem preservados ao retornar à etapa anterior.

---

## CT-048 — Uso de cupom de desconto na etapa de checkout (se aplicável)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | O campo de cupom está disponível na etapa de checkout (não apenas no carrinho) |
| **Prioridade** | Baixa |

**Passos:**
1. Na etapa de pagamento ou resumo, localizar o campo de cupom (se existir separadamente do carrinho)
2. Inserir um cupom válido, se disponível

**Resultado esperado:**
O desconto é aplicado e refletido corretamente no valor final do pedido antes da confirmação.

---

## CT-049 — Abandono do checkout e retomada posterior

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário iniciou o checkout mas não o concluiu |
| **Prioridade** | Baixa |

**Passos:**
1. Avançar até a etapa de pagamento
2. Sair do fluxo (fechar aba ou navegar para outra página) sem finalizar
3. Retornar ao carrinho/checkout posteriormente

**Resultado esperado:**
O sistema deve permitir retomar o processo (ex: itens permanecem no carrinho), sem gerar erro ou pedido duplicado indevido.

---

## CT-050 — Validação de campos obrigatórios não preenchidos no checkout

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em qualquer etapa do checkout com campos obrigatórios |
| **Prioridade** | Alta |

**Passos:**
1. Tentar avançar de etapa sem preencher um campo obrigatório (ex: complemento não obrigatório vs. número do endereço obrigatório)

**Resultado esperado:**
O sistema impede o avanço e destaca claramente o(s) campo(s) pendente(s).

---

## Observações Gerais

- **Limite ético do módulo:** nenhum caso de teste avança até o clique final de "Confirmar pedido" / "Pagar". A execução é sempre interrompida na etapa anterior à confirmação.
- Dados de endereço e identificação utilizados devem ser fictícios.
- Caso o site exija login social (Google/Facebook) em alguma etapa, recomenda-se usar uma conta de teste dedicada, nunca uma conta pessoal real.
- Caso alguma etapa do checkout mude de nome/ordem entre execuções (comum em e-commerces que fazem testes A/B), isso deve ser documentado como observação, e os casos de teste revisados se necessário.
