# Heurísticas para Teste Exploratório

**Projeto:** QA Web - E-commerce

**Uso:** Guia de apoio para qualquer sessão de teste exploratório realizada no projeto, 
independentemente do módulo ou funcionalidade sendo explorada.

---

## 🧠 O que são heurísticas de teste?

Heurísticas são "atalhos mentais" guias práticos que ajudam o testador a lembrar de onde procurar problemas durante uma exploração livre, sem depender de um roteiro fixo de casos de teste. Elas não garantem cobertura completa, mas direcionam a atenção para áreas com maior probabilidade de esconder bugs.

---

## 🔎 Heurística HICCUPPS (Consistência)

Avalia se o sistema é **consistente** com diferentes referências. Ao explorar, pergunte:

| Letra | Consistência com... | Pergunta guia |
|---|---|---|
| **H** | Histórico | O comportamento atual é consistente com versões anteriores da mesma tela/produto? |
| **I** | Imagem (da empresa) | O que estou vendo é condizente com a imagem que a marca quer passar (profissionalismo, confiabilidade)? |
| **C** | Comparável | O comportamento é consistente com produtos/sites similares (concorrentes, outras categorias do mesmo site)? |
| **C** | Claims (alegações) | O que está sendo exibido é consistente com o que é prometido/anunciado (ex: "frete grátis acima de X")? |
| **U** | Usuário | O comportamento atende às expectativas razoáveis de um usuário comum? |
| **P** | Produto | As diferentes partes do produto/sistema são consistentes entre si (preço na PDP = preço no carrinho)? |
| **P** | Propósito | A funcionalidade cumpre o propósito para o qual foi criada? |
| **S** | Padrões (Standards) | O comportamento segue padrões e convenções conhecidas de UX/e-commerce? |

---

## 🧭 Heurística SFDPOT (Dimensões do Produto)

Usada para mapear diferentes ângulos de um produto/funcionalidade antes ou durante a exploração:

| Letra | Dimensão | O que observar |
|---|---|---|
| **S** | Estrutura (Structure) | Do que o sistema é composto? (campos, botões, seções da tela) |
| **F** | Função (Function) | O que o sistema faz? (calcular frete, adicionar ao carrinho) |
| **D** | Dados (Data) | Que dados entram e saem? (CEP, preço, quantidade) — testar valores válidos, inválidos, extremos |
| **P** | Plataforma (Platform) | Em quais ambientes o sistema roda? (navegador, mobile, resolução) |
| **O** | Operações (Operations) | Como o sistema é realmente usado no dia a dia? (fluxos reais de compra) |
| **T** | Tempo (Time) | Como o tempo afeta o sistema? (sessão expirada, estoque mudando, promoção terminando) |

---

## 🎯 Heurísticas de Casos de Borda (Boundary & Error Guessing)

Ao explorar qualquer campo ou funcionalidade, testar deliberadamente:

- **Valores limite:** o menor e o maior valor aceito (ex: 1 unidade x quantidade máxima em estoque)
- **Valores fora do limite:** um a mais e um a menos do que o esperado
- **Valores vazios/nulos:** campo em branco, sem seleção
- **Valores muito longos:** texto excessivamente grande em campos (nome de produto, endereço)
- **Caracteres especiais:** símbolos, emojis, espaços extras
- **Interrupção de fluxo:** atualizar a página no meio de uma ação, clicar em "voltar" do navegador, abrir a mesma tela em duas abas
- **Repetição rápida:** clicar duas vezes rápido em um botão de ação (duplo clique em "Adicionar ao carrinho")

---

## 🚶 Tours de Exploração (Whittaker's Touring Heuristics — adaptado)

Cada "tour" é uma lente diferente para percorrer a mesma funcionalidade:

- **Tour do Dinheiro:** siga o caminho onde há troca de valor (preço, frete, cupom, total) — é onde erros custam mais caro
- **Tour do Turista de Aluguel (Landmark Tour):** visite os pontos mais óbvios e usados da tela, como faria um usuário apressado
- **Tour do Explorador:** vá para áreas menos óbvias, cantos escondidos, links secundários, rodapé
- **Tour do Colecionador:** agrupe elementos parecidos (todos os botões, todos os campos de texto) e teste-os em sequência
- **Tour do Investigador Preguiçoso (Lazy Tester):** tente atalhos — pular etapas, digitar URLs diretamente, usar o botão "voltar" no lugar dos botões da própria tela

---

## 📋 Checklist Rápida de Atenção (uso geral)

Ao final de cada sessão, revisar mentalmente:

- [ ] Testei o caminho feliz (fluxo esperado, sem erros)?
- [ ] Testei ao menos um caminho de erro/inválido?
- [ ] Testei um caso de borda (valor limite, campo vazio, etc.)?
- [ ] Verifiquei consistência entre telas diferentes (ex: PDP x carrinho)?
- [ ] Testei em mais de uma resolução (desktop x mobile)?
- [ ] Registrei tudo que pareceu estranho, mesmo sem certeza se é bug?

---

# 📝 Notas de Sessão (Session Notes)

> Preencher durante ou logo após a execução de qualquer sessão exploratória do projeto.

**Data da sessão:**
**Duração real:**
**Módulo/funcionalidade explorada:**
**Produtos utilizados como exemplo:**

## O que foi testado

-

## O que funcionou bem

-

## Anomalias / comportamentos inesperados encontrados

-

## Dúvidas / pontos que exigem investigação adicional

-
