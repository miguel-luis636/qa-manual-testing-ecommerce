# 5.0 Filtros e Ordenação

**Módulo:** Filtros e Ordenação

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Tipo de teste:** Manual funcional

**Ambiente:** Produção (site público)

---

## CT-051 — Aplicar filtro de categoria

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem de produtos |
| **Prioridade** | Alta |

**Passos:**
1. Acessar uma página de listagem (ex: "Feminino" ou resultado de busca)
2. Selecionar um filtro de categoria (ex: "Vestidos")

**Resultado esperado:**
A listagem é atualizada exibindo apenas produtos pertencentes à categoria selecionada, e o filtro aparece marcado/destacado.

---

## CT-052 — Aplicar filtro de tamanho

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem de produtos |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a página de listagem
2. Selecionar um filtro de tamanho (ex: "M")

**Resultado esperado:**
A listagem exibe apenas produtos disponíveis no tamanho selecionado.

---

## CT-053 — Aplicar filtro de cor

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem de produtos |
| **Prioridade** | Média |

**Passos:**
1. Acessar a página de listagem
2. Selecionar um filtro de cor (ex: "Preto")

**Resultado esperado:**
A listagem exibe apenas produtos disponíveis na cor selecionada.

---

## CT-054 — Aplicar filtro de faixa de preço

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem de produtos |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a página de listagem
2. Selecionar ou inserir uma faixa de preço (ex: R$50 a R$100)

**Resultado esperado:**
A listagem exibe apenas produtos cujo preço está dentro da faixa selecionada.

---

## CT-055 — Aplicar múltiplos filtros combinados

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem de produtos |
| **Prioridade** | Alta |

**Passos:**
1. Selecionar filtro de categoria (ex: "Feminino")
2. Selecionar filtro de cor (ex: "Preto")
3. Selecionar filtro de faixa de preço

**Resultado esperado:**
A listagem exibe apenas produtos que atendem simultaneamente a todos os filtros aplicados (interseção, não união).

---

## CT-056 — Remover um filtro específico

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Dois ou mais filtros estão aplicados |
| **Prioridade** | Alta |

**Passos:**
1. Com múltiplos filtros ativos, remover apenas um deles (via "x" no filtro ou desmarcando a opção)

**Resultado esperado:**
A listagem é atualizada refletindo a remoção apenas do filtro removido; os demais filtros continuam ativos.

---

## CT-057 — Limpar todos os filtros

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Um ou mais filtros estão aplicados |
| **Prioridade** | Média |

**Passos:**
1. Com filtros ativos, clicar em "Limpar filtros" (se disponível)

**Resultado esperado:**
Todos os filtros são removidos de uma vez, e a listagem volta a exibir todos os produtos da categoria original.

---

## CT-058 — Combinação de filtros sem resultados

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem |
| **Prioridade** | Média |

**Passos:**
1. Aplicar uma combinação de filtros pouco provável de retornar resultados (ex: tamanho raro + cor específica + faixa de preço muito baixa)

**Resultado esperado:**
O sistema exibe uma mensagem clara informando que nenhum produto foi encontrado com os filtros aplicados, sem gerar erro ou tela em branco sem explicação.

---

## CT-059 — Persistência de filtros ao acessar um produto e voltar

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Um ou mais filtros estão aplicados na listagem |
| **Prioridade** | Média |

**Passos:**
1. Aplicar filtros na listagem
2. Clicar em um produto para acessar a PDP
3. Clicar em "Voltar" no navegador

**Resultado esperado:**
Os filtros aplicados anteriormente permanecem ativos ao retornar para a listagem.

---

## CT-060 — Persistência de filtros ao recarregar a página

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Um ou mais filtros estão aplicados (refletidos na URL, se aplicável) |
| **Prioridade** | Baixa |

**Passos:**
1. Aplicar filtros na listagem
2. Recarregar a página (F5)

**Resultado esperado:**
Caso os filtros estejam refletidos na URL, eles devem permanecer aplicados após o reload. Caso contrário, o comportamento deve ser documentado como observação.

---

## CT-061 — Ordenação por menor preço

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem com múltiplos produtos |
| **Prioridade** | Alta |

**Passos:**
1. Selecionar a opção de ordenação "Menor preço"

**Resultado esperado:**
Os produtos são reordenados corretamente do menor para o maior preço.

---

## CT-062 — Ordenação por maior preço

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem com múltiplos produtos |
| **Prioridade** | Alta |

**Passos:**
1. Selecionar a opção de ordenação "Maior preço"

**Resultado esperado:**
Os produtos são reordenados corretamente do maior para o menor preço.

---

## CT-063 — Ordenação por lançamentos/novidades

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem |
| **Prioridade** | Média |

**Passos:**
1. Selecionar a opção de ordenação "Novidades" ou "Lançamentos" (se disponível)

**Resultado esperado:**
Os produtos são reordenados priorizando os itens adicionados mais recentemente ao catálogo.

---

## CT-064 — Ordenação por relevância (padrão)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem |
| **Prioridade** | Baixa |

**Passos:**
1. Aplicar uma ordenação diferente (ex: menor preço)
2. Retornar para a ordenação padrão ("Relevância" ou similar)

**Resultado esperado:**
A listagem retorna à ordenação original/padrão do site sem erros.

---

## CT-065 — Combinação de filtros com ordenação

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está em uma página de listagem |
| **Prioridade** | Média |

**Passos:**
1. Aplicar um filtro (ex: categoria "Vestidos")
2. Aplicar uma ordenação (ex: "Menor preço")

**Resultado esperado:**
O filtro e a ordenação funcionam simultaneamente: a listagem exibe apenas produtos filtrados, já ordenados conforme critério selecionado.

---

## CT-066 — Contador de produtos filtrados

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Filtros estão sendo aplicados |
| **Prioridade** | Baixa |

**Passos:**
1. Aplicar um ou mais filtros
2. Observar se há um contador de "X produtos encontrados" ou similar

**Resultado esperado:**
Caso exista essa contagem, ela deve refletir corretamente a quantidade real de produtos exibidos após o(s) filtro(s) aplicado(s).

---

## Observações Gerais

- Recomenda-se testar filtros e ordenação em pelo menos duas categorias diferentes do site (ex: "Feminino" e "Masculino"), já que a disponibilidade de filtros pode variar entre categorias
- Comportamentos de UX sem impacto funcional (ex: ausência de "Limpar filtros") devem ser registrados como observação, não necessariamente como bug
- Testar também em resolução mobile (via DevTools), pois a interface de filtros costuma mudar de layout (menu lateral vs. modal/drawer) entre desktop e mobile
