# Resultados de Execução — Módulo 3.0 Carrinho de Compras

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
| Bugs abertos a partir da execução | 1 (BUG-20260721-005) |

---

## 📋 Resultado por Caso de Teste

| ID | Caso de Teste | Resultado | Observação |
|---|---|:---:|---|
| CT-025 | Adicionar produto ao carrinho | ✅ Passou | — |
| CT-026 | Tentar adicionar produto sem selecionar variação obrigatória | ✅ Passou | — |
| CT-027 | Alterar quantidade de um item no carrinho | ✅ Passou | — |
| CT-028 | Remover item do carrinho | ✅ Passou | — |
| CT-029 | Visualizar carrinho vazio | ✅ Passou | — |
| CT-030 | Aplicar cupom de desconto válido | ✅ Passou | — |
| CT-031 | Aplicar cupom inválido ou expirado | ✅ Passou | — |
| CT-032 | Persistência do carrinho para usuário logado | ✅ Passou | Ícone do carrinho não exibe o número de itens imediatamente após o login, mesmo com produtos salvos na conta — número só aparece corretamente após visitar a página do carrinho (ver BUG-20260721-005) |
| CT-033 | Persistência do carrinho para usuário não logado (guest) | ✅ Passou | — |
| CT-034 | Quantidade acima do estoque disponível | ✅ Passou | — |
| CT-035 | Produto esgotado durante navegação no carrinho | ⚪ Não testado | Não foi possível reproduzir o cenário de produto ficando esgotado durante a sessão de teste |
| CT-036 | Resumo de valores no carrinho (subtotal, frete estimado, total) | ✅ Passou | — |
| CT-037 | Continuar comprando a partir do carrinho | ✅ Passou | — |

**Legenda:** ✅ Passou · ❌ Não passou · ⚪ Não testado / Não aplicável

---

## 🐞 Bugs Identificados Nesta Execução

| ID | Título | Severidade | Origem |
|---|---|---|---|
| BUG-20260721-005 | Contador do ícone do carrinho não atualiza imediatamente após login | S3 — Médio | CT-032 |

---

## 📝 Observações Gerais da Sessão

- O caso CT-032 foi considerado aprovado (o carrinho de fato persiste corretamente para o usuário logado — os produtos não são perdidos), porém a execução revelou uma inconsistência visual no contador do ícone do carrinho, registrada como bug separado (BUG-20260721-005), já que representa um problema de exibição, não de persistência de dados em si.
- O caso CT-035 (produto esgotado durante navegação no carrinho) não foi testado nesta rodada, por não ter sido possível localizar ou forçar um cenário de produto esgotando durante a sessão de teste. Recomenda-se nova tentativa em execução futura, possivelmente monitorando um produto com estoque visivelmente baixo ("últimas unidades").
- Nenhum outro comportamento inesperado foi identificado nos demais casos do módulo.
 
