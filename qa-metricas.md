# 📊 Relatório de Métricas de QA — QA Web E-commerce

> Gerado em: 21/07/2026
> 

---

## 🔹 Visão Geral

| Métrica | Valor |
|--------|-------|
| Total de documentos analisados | 15 |
| Relatórios de bugs / melhorias | 3 arquivos (5 achados: 3 bugs + 2 melhorias) |
| Cenários de teste (módulos com CTs formais) | 5 (66 casos ao todo) |
| Relatórios de execução (métricas por módulo) | 5 |
| Plano de testes | 1 (`Plano_de_Testes.md`) |
| Testes exploratórios documentados | 0 executados (guia de heurísticas presente, sessões pendentes) |
| Cobertura de fluxos planejados no escopo | 5 de 7 (71%) — PDP e Frete/CEP sem arquivo de casos de teste no repo |
| Bugs críticos (S1) abertos | 0 |

---

## 🧪 Resultado dos Testes Regressivos

| Módulo | ✅ Passou | ❌ Falhou | 🚧 Não Testado | Taxa de Passagem |
|--------|:---:|:---:|:---:|:---:|
| 1.0 Cadastro e Login | 12 | 1 | 0 | 92,3% |
| 2.0 Busca de Produtos | 9 | 0 | 2 | 100% |
| 3.0 Carrinho de Compras | 12 | 0 | 1 | 100% |
| 4.0 Checkout | 12 | 0 | 1 | 100% |
| 5.0 Filtros e Ordenação | 15 | 0 | 1 | 100% |
| **Total** | **60** | **1** | **5** | **98,4%** |

**Distribuição geral (66 casos planejados):**
```
PASSOU     ████████████████████████████████████ 60 (90,9%)
FALHOU     █ 1 (1,5%)
NÃO TEST.  ███ 5 (7,6%)
```

**Taxa de passagem por módulo (%):**
```
1.0 Cadastro     ██████████████████ 92,3%
2.0 Busca        ████████████████████ 100%
3.0 Carrinho     ████████████████████ 100%
4.0 Checkout     ████████████████████ 100%
5.0 Filtros      ████████████████████ 100%
```
---

### Melhorias de Usabilidade

| ID / Nome | Prioridade | Módulo |
|-----------|:---:|--------|
| MELHORIA-20260721-001 — Erro de cadastro sem indicar campo | Alta | 1.0 Cadastro e Login |
| MELHORIA-20260721-002 — Recuperação de senha sem feedback visual | Média | 1.0 Cadastro e Login |

**Distribuição por severidade (bugs):**
```
S1 CRÍTICO  (nenhum)
S2 ALTO     (nenhum)
S3 MÉDIO    ███████████████████████████████████████████████████ 3 (100%)
S4 BAIXO    (nenhum)
```

## 📌 Resumo Executivo

O projeto demonstra uma taxa de sucesso agregada de 98,4% sobre 61 casos executados em 5 módulos, sem nenhum bug crítico ou de alta severidade identificado — um resultado sólido para um portfólio de QA júnior. Entretanto, existem gaps de rastreabilidade (2 bugs citados nas métricas mas sem arquivo correspondente) e de cobertura (2 dos 7 módulos do escopo — PDP e Frete — ainda sem nenhum caso de teste documentado), além de uma tabela de progresso no README desatualizada em relação aos resultados já obtidos.
