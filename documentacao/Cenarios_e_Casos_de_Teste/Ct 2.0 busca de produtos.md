# 2.0 Busca de Produtos

**Módulo:** Busca de Produtos

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Tipo de teste:** Manual funcional

**Ambiente:** Produção (site público)

---

## CT-014 — Busca por termo válido e específico

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o site do e-commerce
2. Clicar no campo de busca
3. Digitar um termo específico (ex: "vestido floral")
4. Pressionar Enter ou clicar no ícone de busca

**Resultado esperado:**
O sistema exibe uma lista de produtos relacionados ao termo buscado, com a quantidade de resultados encontrados visível na página.

---

## CT-015 — Busca por termo genérico

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Média |

**Passos:**
1. Acessar o campo de busca
2. Digitar um termo genérico (ex: "camisa")
3. Pressionar Enter

**Resultado esperado:**
O sistema retorna um grande volume de resultados relacionados, com paginação ou carregamento incremental funcionando corretamente.

---

## CT-016 — Busca por termo inexistente

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o campo de busca
2. Digitar um termo sem correspondência no catálogo (ex: "xzqwerty123")
3. Pressionar Enter

**Resultado esperado:**
O sistema exibe uma mensagem clara informando que nenhum produto foi encontrado, idealmente sugerindo categorias populares ou produtos relacionados como alternativa.

---

## CT-017 — Busca com campo vazio

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Baixa |

**Passos:**
1. Clicar no campo de busca sem digitar nada
2. Pressionar Enter ou clicar no ícone de busca

**Resultado esperado:**
O sistema não deve retornar erro; deve manter o usuário na página atual ou exibir uma mensagem apropriada solicitando que um termo seja digitado.

---

## CT-018 — Busca com caracteres especiais

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Média |

**Passos:**
1. Acessar o campo de busca
2. Digitar caracteres especiais (ex: `%$#@!*`)
3. Pressionar Enter

**Resultado esperado:**
O sistema trata a entrada sem gerar erro técnico (tela quebrada, erro 500, etc.), exibindo resultado vazio ou mensagem adequada.

---

## CT-019 — Busca com termo em letras maiúsculas/minúsculas

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Baixa |

**Passos:**
1. Buscar um termo em maiúsculas (ex: "VESTIDO")
2. Repetir a busca com o mesmo termo em minúsculas (ex: "vestido")

**Resultado esperado:**
Ambas as buscas devem retornar os mesmos resultados, indicando que a busca não é case-sensitive.

---

## CT-020 — Busca com termo contendo erro de digitação

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Média |

**Passos:**
1. Digitar um termo com pequeno erro de digitação (ex: "vestdo" em vez de "vestido")
2. Pressionar Enter

**Resultado esperado:**
O sistema idealmente sugere a correção ("Você quis dizer: vestido?") ou já retorna resultados aproximados. Caso não haja essa funcionalidade, o comportamento deve ser documentado como observação, não necessariamente como bug.

---

## CT-021 — Sugestões automáticas durante a digitação (autocomplete)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página inicial do site |
| **Prioridade** | Média |

**Passos:**
1. Clicar no campo de busca
2. Começar a digitar um termo parcial (ex: "bols")
3. Observar o comportamento do campo antes de pressionar Enter

**Resultado esperado:**
Caso o site possua autocomplete, sugestões relevantes devem aparecer (produtos, categorias ou termos populares relacionados ao texto digitado).

---

## CT-022 — Busca por código/SKU de produto (não é aplicável)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário possui um código de produto válido |
| **Prioridade** | Baixa |

**Passos:**
1. Digitar o código/SKU de um produto conhecido no campo de busca
2. Pressionar Enter

**Resultado esperado:**
Caso o site suporte busca por código, o produto correspondente deve ser exibido diretamente nos resultados.

---

## CT-023 — Clicar em um resultado da busca

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Uma busca válida já retornou resultados |
| **Prioridade** | Alta |

**Passos:**
1. Realizar uma busca válida
2. Clicar em um dos produtos retornados na listagem

**Resultado esperado:**
O usuário é direcionado corretamente para a página de detalhes (PDP) do produto selecionado, com informações consistentes com o que foi exibido na busca.

---

## CT-024 — Histórico ou buscas recentes (não é aplicável)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário já realizou buscas anteriormente na mesma sessão |
| **Prioridade** | Baixa |

**Passos:**
1. Realizar uma busca por um termo
2. Clicar novamente no campo de busca (sem recarregar a página)

**Resultado esperado:**
Caso o site tenha essa funcionalidade, buscas recentes devem ser exibidas como sugestão. Caso não tenha, não deve ser considerado bug — apenas ausência de funcionalidade.

---

## Observações Gerais

- Termos de busca utilizados nos testes devem ser genéricos e não relacionados a dados pessoais
- Comportamentos de UX que não geram erro técnico (ex: ausência de autocomplete) devem ser registrados como observação/sugestão de melhoria, não necessariamente como bug — a menos que quebrem a funcionalidade
- Recomenda-se testar a busca tanto em desktop quanto em resolução mobile (via DevTools), já que o campo de busca costuma ter comportamento diferente entre os dois layouts
