 Test Plan — QA Web E-commerce
 
## 1. Identificação
 
| Campo | Detalhes |
|---|---|
| **Projeto** | QA Web - E-commerce |
| **Aplicação sob teste (AUT)** | Site de e-commerce (produção, terceiro) |
| **Tipo** | E-commerce |
| **Responsável pelo plano** | Miguel Luis — QA Júnior |
| **Versão do documento** | 1.0 |
| **Data** | Julho/2026 |
 
---
 
## 2. Objetivo
 
Este documento define a estratégia, o escopo, os critérios e os recursos utilizados para a execução dos testes manuais funcionais no site de um e-commerce de moda, com o propósito de demonstrar competências práticas de QA em um ambiente de e-commerce real, para fins de portfólio profissional.
 
---
 
## 3. Escopo
 
### 3.1 Dentro do escopo
 
| Módulo | Descrição |
|---|---|
| Cadastro e Login | Criação de conta, autenticação, recuperação de senha |
| Busca de Produtos | Busca textual, resultados vazios, sugestões |
| Filtros e Ordenação | Filtros de categoria, tamanho, cor, preço; ordenação de resultados |
| Página de Produto (PDP) | Exibição de imagens, variações, disponibilidade, informações do produto |
| Carrinho de Compras | Adição, remoção, alteração de quantidade, cupom, persistência |
| Simulação de Frete (CEP) | Cálculo de frete por CEP válido/inválido, opções de entrega |
| Checkout  (sem conclusão da compra)| Identificação, endereço, resumo do pedido, seleção de forma de pagamento |
 
### 3.2 Fora do escopo
 
- Finalização real de compras / confirmação de pagamento
- Testes de performance e carga
- Testes de segurança (pentest, exploração de vulnerabilidades)
- Automação de testes (Selenium, Cypress, Robot Framework)
- Testes de API ou sistemas internos da empresa
- Testes em dispositivos físicos móveis (apenas emulação via DevTools)
---
 
## 4. Estratégia de Teste
 
### 4.1 Abordagem
 
- **Teste manual funcional**, guiado por casos de teste formais escritos em Gherkin (Dado/Quando/Então)
- **Teste exploratório complementar**, para identificar comportamentos não previstos nos cenários formais
- Testes executados em ambiente de **produção pública**, sem nenhuma interferência ativa na aplicação (sem automação, scraping ou carga)
### 4.2 Tipos de teste aplicados
 
| Tipo | Aplicado? | Observação |
|---|:---:|---|
| Funcional | ✅ | Núcleo do projeto |
| Exploratório | ✅ | Complementar aos casos formais |
| Regressão | ⚠️ Parcial | Reexecução pontual após mudanças perceptíveis no site |
| Responsividade | ✅ | Via Chrome DevTools |
| Usabilidade | ✅ | Observações qualitativas registradas nos bugs/notas |
| Performance | ❌ | Fora do escopo |
| Segurança | ❌ | Fora do escopo |
| Automação | ❌ | Fora do escopo |
 
### 4.3 Dados de teste
 
- Todos os dados pessoais utilizados (nome, e-mail, telefone) serão **fictícios**
- CPFs, quando necessários, seguirão apenas formato válido de teste, sem pertencer a pessoas reais
- Nenhum cartão de crédito real será inserido em nenhuma etapa
- CEPs utilizados serão reais (dado público), mas sem associação a endereço pessoal do testador quando possível
---
 
## 5. Critérios de Entrada e Saída
 
### 5.1 Critérios de entrada
- Casos de teste elaborados e revisados para o módulo a ser testado
- Ambiente de teste (navegador, resolução) definido e disponível
- Site do e-commerce acessível e estável no momento da execução
### 5.2 Critérios de saída
- Todos os casos de teste planejados para o módulo foram executados
- Todos os bugs encontrados foram documentados com evidência
- A tabela de progresso no README foi atualizada
### 5.3 Critérios de suspensão
- Indisponibilidade do site (erro 5xx, timeout persistente)
- Alterações estruturais grandes no site que invalidem os casos de teste vigentes (nesse caso, os casos são revisados antes de continuar)
---
 
## 5. Ambiente e Ferramentas
 
| Item | Detalhe |
|---|---|
| Ambiente | Produção pública (site de terceiro) |
| Navegador principal | Google Chrome (última versão estável) |
| Navegador secundário | Mozilla Firefox |
| Sistema Operacional | Windows 11 |
| Resoluções | Desktop 1920x1080, Mobile simulado (DevTools) |
| Documentação | Markdown + Git/GitHub |
| Evidências | Capturas de tela armazenadas em `/evidencias` |
 
---
 
## 7. Papéis e Responsabilidades
 
| Papel | Responsável | Atividades |
|---|---|---|
| QA / Testador | Miguel Luis | Planejamento, elaboração de casos, execução, documentação de bugs |
 
---
 
## 8. Riscos do Projeto
 
| Risco | Impacto | Mitigação |
|---|---|---|
| Site em produção pode mudar sem aviso, invalidando casos de teste | Médio | Casos de teste revisados periodicamente; versionamento no Git permite rastrear mudanças |
| Interpretação incorreta de comportamento esperado (não há especificação oficial disponível) | Médio | Basear expectativas em padrões de UX de e-commerce e senso comum de usuário |
| Indisponibilidade temporária do site | Baixo | Reagendar execução; não é um risco controlável pelo testador |
| Uso indevido de dados reais por engano | Alto (ético) | Checklist de dados fictícios revisado antes de cada execução |
 
---
 
## 9. Critérios de Severidade e Prioridade (referência)
 
| Severidade | Critério |
|---|---|
| S1 — Crítico | Bloqueia fluxo principal |
| S2 — Alto | Funcionalidade falha, mas há workaround |
| S3 — Médio | Inconsistência sem bloqueio |
| S4 — Baixo | Cosmético |
 
| Prioridade | Critério |
|---|---|
| P0 — Urgente | Crítico e reproduzível |
| P1 — Alta | Impacto relevante |
| P2 — Média | Importante, sem urgência |
| P3 — Baixa | Backlog |
 
*(Detalhamento completo dos critérios de bug reporting está no `TEMPLATE-bug-report.md`.)*
 
---
 
## 10. Premissas
 
- O testador não possui acesso a documentação interna, requisitos ou especificações da empresa — as expectativas são baseadas em comportamento padrão esperado de e-commerce e boas práticas de UX
- O projeto não tem qualquer vínculo oficial com a empresa proprietária do site testado.
- Nenhuma etapa de pagamento será concluída em nenhum cenário
---
 
## 11. Aprovação
 
Como projeto de portfólio individual, este plano é autoaprovado pelo autor antes do início da execução dos testes.
 
**Autor:** Miguel Luis
**LinkedIn:** [linkedin.com/in/miguel-luisatf](https://www.linkedin.com/in/miguel-luisatf/)
