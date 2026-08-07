# Resultado Geral dos Testes — QA Web E-commerce
 
**Projeto:** QA Web - E-commerce
 
**Aplicação:** Site do e-commerce testado (produção, terceiro)
 
**Ambiente:** Google Chrome (última versão), Windows 11, Desktop
 
**Executor:** Miguel Luis
 
**Data de consolidação:** 21/07/2026
 
---
 
## 📊 Métricas Gerais Consolidadas (Módulos 1 a 5)
 
| Métrica | Valor |
|---|---|
| Total de casos de teste planejados | 66 |
| Total de casos executados | 61 |
| Total de casos não testados (N/A) | 5 |
| Total de casos aprovados (Pass) | 60 |
| Total de casos reprovados (Fail) | 1 |
| **Taxa de sucesso (sobre executados)** | **98,4%** |
| Total de bugs identificados | 3 |
| Total de melhorias de usabilidade identificadas | 2 |
 
---
 
## 📋 Resumo por Módulo
 
| Módulo | Planejados | Executados | Aprovados | Reprovados | N/A | Taxa de Sucesso | Bugs | Melhorias |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1.0 Cadastro e Login | 13 | 13 | 12 | 1 | 0 | 92,3% | 0 | 2 |
| 2.0 Busca de Produtos | 11 | 9 | 9 | 0 | 2 | 100% | 1 | 0 |
| 3.0 Carrinho de Compras | 13 | 12 | 12 | 0 | 1 | 100% | 1 | 0 |
| 4.0 Checkout | 13 | 12 | 12 | 0 | 1 | 100% | 0 | 0 |
| 5.0 Filtros e Ordenação | 16 | 15 | 15 | 0 | 1 | 100% | 0 | 0 |
| **Total** | **66** | **61** | **60** | **1** | **5** | **98,4%** | **3** | **2** |
 
---
 
## 🐞 Bugs Identificados (Consolidado)
 
| ID | Título | Módulo de Origem | Severidade | Status |
|---|---|---|:---:|:---:|
| BUG-20260721-005 | Contador do ícone do carrinho não atualiza imediatamente após login | 3.0 Carrinho de Compras | S3 — Médio | 🔴 Novo |
 
---
 
## 💡 Melhorias de Usabilidade Identificadas (Consolidado)
 
| ID | Título | Módulo de Origem | Prioridade Sugerida | Status |
|---|---|---|:---:|:---:|
| MELHORIA-20260721-001 | Erro de "dado inválido" no cadastro sem indicar qual campo | 1.0 Cadastro e Login | Alta | 🟡 Identificada |
| MELHORIA-20260721-002 | Recuperação de senha sem feedback visual para dado inexistente | 1.0 Cadastro e Login | Média | 🟡 Identificada |
 
---
 
## ❌ Caso Reprovado (Detalhe)
 
| ID | Caso de Teste | Módulo | Motivo da Reprovação |
|---|---|---|---|
| CT-011 | Recuperação de senha com e-mail não cadastrado | 1.0 Cadastro e Login | Sistema aceita CPF inexistente sem alertar o usuário (ver MELHORIA-20260721-002) |
 
---
 
## ⚪ Casos Não Testados (Detalhe)
 
| ID | Caso de Teste | Módulo | Motivo |
|---|---|---|---|
| CT-022 | Busca por código/SKU de produto | 2.0 Busca de Produtos | Funcionalidade não identificada/aplicável |
| CT-024 | Histórico ou buscas recentes | 2.0 Busca de Produtos | Funcionalidade não identificada/aplicável |
| CT-035 | Produto esgotado durante navegação no carrinho | 3.0 Carrinho de Compras | Não foi possível reproduzir o cenário na sessão de teste |
| CT-043 | Seleção entre diferentes opções de frete | 4.0 Checkout | Apenas uma opção de frete disponível no momento da execução |
| CT-054 | Aplicar filtro de faixa de preço | 5.0 Filtros e Ordenação | Funcionalidade descrita não existe — site oferece apenas ordenação por maior/menor preço, não filtro de intervalo customizável |
 
---
 
## 📝 Conclusões Gerais
 
- O projeto atingiu uma **taxa de sucesso de 98,4%** sobre os casos executados nos 5 módulos com casos de teste formais, com apenas 1 caso reprovado (CT-011) e 3 bugs funcionais identificados, todos de severidade média (S3).
- Nenhum bug crítico (S1) ou alto (S2) foi identificado até o momento nesta rodada de testes.
- As 2 melhorias de usabilidade identificadas estão concentradas no módulo de Cadastro e Login, sugerindo que esse é o ponto de maior oportunidade de refinamento de UX no fluxo avaliado.
- 5 casos não puderam ser testados por motivos variados (funcionalidade inexistente, cenário não reproduzível, ou indisponibilidade momentânea) — nenhum desses casos foi computado como reprovação, mas permanecem como pendências para reavaliação futura.
