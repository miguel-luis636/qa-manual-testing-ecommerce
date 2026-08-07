# Resultados de Execução — Módulo 4.0 Checkout (sem conclusão de compra)

**Data da execução:** 21/07/2026

**Ambiente:** Google Chrome (última versão), Windows 11, Desktop

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Executor:** Miguel Luis

---

## 📊 Métricas do Módulo

| Métrica | Valor |
|---|---|
| Total de casos de teste planejados | 13 |
| Casos executados | 12 |
| Casos não testados (N/A) | 1 |
| Casos aprovados (Pass) | 12 |
| Casos reprovados (Fail) | 0 |
| Taxa de sucesso (sobre executados) | 100% |
| Bugs abertos a partir da execução | 0 |

---

## 📋 Resultado por Caso de Teste

| ID | Caso de Teste | Resultado | Observação |
|---|---|:---:|---|
| CT-038 | Iniciar checkout com carrinho preenchido | ✅ Passou | — |
| CT-039 | Checkout exige login ou identificação | ✅ Passou | — |
| CT-040 | Seleção de endereço de entrega já cadastrado | ✅ Passou | — |
| CT-041 | Cadastro de novo endereço durante o checkout | ✅ Passou | — |
| CT-042 | Cálculo de frete durante o checkout | ✅ Passou | — |
| CT-043 | Seleção entre diferentes opções de frete | ⚪ Não testado | Não foi possível validar — apenas uma opção de frete disponível no momento da execução, ou cenário não identificado |
| CT-044 | Visualizar resumo do pedido antes do pagamento | ✅ Passou | — |
| CT-045 | Seleção da forma de pagamento (sem finalizar) | ✅ Passou | — |
| CT-046 | Alternar entre formas de pagamento disponíveis | ✅ Passou | — |
| CT-047 | Voltar etapa no checkout sem perder dados preenchidos | ✅ Passou | — |
| CT-048 | Uso de cupom de desconto na etapa de checkout | ✅ Passou | — |
| CT-049 | Abandono do checkout e retomada posterior | ✅ Passou | — |
| CT-050 | Validação de campos obrigatórios não preenchidos no checkout | ✅ Passou | — |

**Legenda:** ✅ Passou · ❌ Não passou · ⚪ Não testado / Não aplicável

---

## 🐞 Bugs Identificados Nesta Execução

Nenhum bug identificado nesta execução.

---

## 📝 Observações Gerais da Sessão

- Este foi o módulo com melhor resultado até o momento no projeto: 12 de 12 casos executados aprovados, sem nenhum bug ou inconsistência identificada.
- O caso CT-043 (seleção entre diferentes opções de frete) não foi testado, pois não foi possível confirmar a disponibilidade de múltiplas opções de frete (ex: padrão x expresso) no momento da execução. Recomenda-se reavaliar esse caso futuramente, testando com CEPs de diferentes regiões, já que a disponibilidade de opções de frete pode variar conforme o endereço de entrega.
- Como reforçado no plano de testes e no README do projeto, nenhuma etapa deste módulo avançou até a confirmação/finalização real do pedido — a execução foi sempre interrompida na etapa anterior à submissão do pagamento.
 
