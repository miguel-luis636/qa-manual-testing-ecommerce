# Resultados de Execução — Módulo 5.0 Filtros e Ordenação

**Data da execução:** 21/07/2026

**Ambiente:** Google Chrome (última versão), Windows 11, Desktop

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Executor:** Miguel Luis

---

## 📊 Métricas do Módulo

| Métrica | Valor |
|---|---|
| Total de casos de teste planejados | 16 |
| Casos executados | 15 |
| Casos não testados (N/A) | 1 |
| Casos aprovados (Pass) | 15 |
| Casos reprovados (Fail) | 0 |
| Taxa de sucesso (sobre executados) | 100% |
| Bugs abertos a partir da execução | 0 |

---

## 📋 Resultado por Caso de Teste

| ID | Caso de Teste | Resultado | Observação |
|---|---|:---:|---|
| CT-051 | Aplicar filtro de categoria | ✅ Passou | — |
| CT-052 | Aplicar filtro de tamanho | ✅ Passou | — |
| CT-053 | Aplicar filtro de cor | ✅ Passou | — |
| CT-054 | Aplicar filtro de faixa de preço | ⚪ Não testado | Funcionalidade não existe da forma descrita no caso de teste — o site não permite inserir uma faixa de preço customizada, apenas oferece ordenação por "maior preço", "menor preço" ou "mais vendido" |
| CT-055 | Aplicar múltiplos filtros combinados | ✅ Passou | — |
| CT-056 | Remover um filtro específico | ✅ Passou | — |
| CT-057 | Limpar todos os filtros | ✅ Passou | — |
| CT-058 | Combinação de filtros sem resultados | ✅ Passou | — |
| CT-059 | Persistência de filtros ao acessar um produto e voltar | ✅ Passou | — |
| CT-060 | Persistência de filtros ao recarregar a página | ✅ Passou | — |
| CT-061 | Ordenação por menor preço | ✅ Passou | — |
| CT-062 | Ordenação por maior preço | ✅ Passou | — |
| CT-063 | Ordenação por lançamentos/novidades | ✅ Passou | — |
| CT-064 | Ordenação por relevância (padrão) | ✅ Passou | — |
| CT-065 | Combinação de filtros com ordenação | ✅ Passou | — |
| CT-066 | Contador de produtos filtrados | ✅ Passou | — |

**Legenda:** ✅ Passou · ❌ Não passou · ⚪ Não testado / Não aplicável

---

## 🐞 Bugs Identificados Nesta Execução

Nenhum bug identificado nesta execução.

---

## 📝 Observações Gerais da Sessão

- O caso CT-054 foi marcado como **não testado**, não por falha de execução, mas porque o caso de teste original previa uma funcionalidade (inserção de uma faixa de preço customizada, ex: "R$50 a R$100") que **não existe no site conforme implementado**. Na prática, o site oferece apenas as opções de ordenação "Maior preço", "Menor preço" e "Mais vendido" — não um filtro de intervalo de preço.
- **Ação recomendada:** revisar o caso de teste CT-054 no arquivo `5.0 Filtros e Ordenação.md`, ajustando sua descrição para refletir a funcionalidade real do site (ordenação por preço, já coberta pelos casos CT-061 e CT-062), em vez de um filtro de faixa que não existe. Isso evita que o caso continue aparecendo como "não testável" em execuções futuras.
- Nenhum outro comportamento inesperado foi identificado nos demais casos do módulo — resultado 100% de aprovação sobre os casos executados, sem nenhum bug encontrado.
