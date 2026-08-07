# QA Web - E-commerce de Moda

![Status](https://img.shields.io/badge/status-em%20andamento-yellow)
![Tipo](https://img.shields.io/badge/tipo-teste%20manual-blue)
![Escopo](https://img.shields.io/badge/escopo-educacional-lightgrey)

## 📌 Sobre o projeto

Este repositório reúne a documentação de testes manuais realizados no site de um grande e-commerce de moda, com foco na validação das principais funcionalidades sob a perspectiva de Qualidade de Software (QA).

O objetivo é demonstrar habilidades em planejamento, elaboração de casos de teste, execução de testes, documentação de evidências e reporte de bugs, utilizando boas práticas da área de Quality Assurance — simulando o dia a dia de um(a) QA júnior atuando em um time de e-commerce.

> **Observação:** Este projeto possui caráter exclusivamente educacional e de portfólio.

---

## 🎯 Objetivo

Realizar testes funcionais manuais nas principais funcionalidades de um e-commerce de moda, documentando:

- Plano de testes
- Casos de teste
- Evidências de execução
- Bugs encontrados (quando aplicável), com severidade e prioridade classificadas

Este projeto busca refletir um processo de QA real: planejar antes de testar, documentar de forma rastreável, e comunicar problemas de forma clara e acionável para um time de desenvolvimento.

---

## 📋 Escopo

As funcionalidades avaliadas incluem:

- Cadastro e Login
- Busca de produtos
- Filtros e ordenação
- Página de produto
- Carrinho de compras
- Simulação de frete (CEP)
- Fluxo de checkout (sem conclusão da compra)

### Fora do escopo

Este projeto **não contempla**:

- Finalização de compras reais
- Processamento de pagamentos
- Testes de carga ou performance
- Testes de segurança (Pentest)
- Automação de testes
- APIs ou sistemas internos da empresa

> A decisão de manter o projeto 100% manual (sem automação ou testes de carga) é intencional: o site é um ambiente de produção real de terceiros, e testes automatizados/carga exigiriam autorização explícita da empresa, o que está fora do escopo de um projeto de portfólio.

---

## 📊 Progresso dos Módulos Testados

| Módulo | Casos de Teste | Status | Bugs Encontrados |
|---|:---:|:---:|:---:|
| Cadastro e Login | 13 | ⚠️ Concluído com achados | 2 melhorias (MELHORIA-001, MELHORIA-002) |
| Busca de Produtos | 11 | ⚠️ Concluído com achados |  |
| Carrinho de Compras | 13 | ⚠️ Concluído com achados |  |
| Checkout (até pagamento) | 13 | ✅ Concluído | - |
| Filtros e Ordenação | 16 | ✅ Concluído | - |


**Legenda:** 🔲 Não iniciado · 🟡 Em andamento · ✅ Concluído · ⚠️ Concluído com achados

> Resultado geral consolidado (módulos 1 a 5): **98,4% de taxa de sucesso** sobre 61 casos executados, 3 bugs e 2 melhorias identificados, nenhum de severidade crítica ou alta. Ver [`documentacao/Resultado_dos_Testes.md`](./documentacao/Resultado_dos_Testes.md) para o detalhamento completo.
> Esta tabela é atualizada conforme a execução avança. Cada módulo concluído linka para seu arquivo de casos de teste correspondente em `documentacao/Cenarios_e_Casos_de_Teste/`.

---

## 🖥️ Ambiente de Testes

| Item                | Detalhes                |
| ------------------- | ------------------------ |
| Sistema Operacional | Windows 11               |
| Navegador Principal | Google Chrome (última versão estável) |
| Navegador Secundário| Mozilla Firefox (testes pontuais) |
| Tipo de Teste       | Testes Manuais Funcionais e Exploratórios |
| Ambiente            | Produção (Site Público de terceiro) |
| Resoluções testadas | Desktop (1920x1080) e Mobile (simulado via DevTools) |

---

## 🛠️ Ferramentas Utilizadas

| Ferramenta | Finalidade |
|---|---|
| Markdown | Documentação de casos de teste e bugs |
| Git & GitHub | Versionamento e portfólio público |
| Google Chrome + DevTools | Execução dos testes e inspeção de elementos/console |
| Ferramenta de captura de tela | Evidências visuais dos testes e bugs |

---

## 🔍 Metodologia

1. **Planejamento** — definição de escopo, riscos e critérios em `documentacao/Plano_de_Testes.md`
2. **Elaboração dos casos de teste** — cenários formais (módulos 1 a 5) e sessões exploratórias guiadas por heurísticas (módulos 6 e 7), cobrindo caminho feliz, caminhos alternativos e casos de borda
3. **Execução manual** — navegação real no site, seguindo os cenários definidos
4. **Registro de evidências** — prints das telas relevantes, salvos em `/evidencias`
5. **Reporte de bugs e melhorias** — sempre que um cenário falha ou revela um ponto de UX a melhorar, é gerado um relatório padronizado em `/bug-reports`, com severidade/prioridade (bugs) ou prioridade sugerida (melhorias)
6. **Atualização de progresso** — a tabela de progresso é atualizada a cada módulo concluído, com base nas métricas consolidadas em `documentacao/Resultado_dos_Testes.md`

---

## 📂 Estrutura do Repositório

```text
qa-web-ecommerce/
│
├── README.md
│
├── bug-reports/

│
├── documentacao/
│   ├── Plano_de_Testes.md
│   ├── Resultado_dos_Testes.md
│   └── Cenarios_e_Casos_de_Teste/
│       ├── 1.0 Cadastro e Login.md
│       ├── 2.0 Busca de Produtos.md
│       ├── 3.0 Carrinho de Compras.md
│       ├── 4.0 Checkout (sem conclusão da compra).md
│       ├── 5.0 Filtros e Ordenação.md
│       └── Teste-Exploratorio.md
│
├── metricas/
│   ├── 1.0 Cadastro e Login.md
│   ├── 2.0 Busca de Produtos.md
│   ├── 3.0 Carrinho de Compras.md
│   ├── 4.0 Checkout.md
│   └── 5.0 Filtros e Ordenação.md

```

---

## 🚦 Critérios de Severidade e Prioridade

| Severidade | Critério |
|---|---|
| **S1 — Crítico** | Bloqueia fluxo principal (ex: impossível adicionar item ao carrinho) |
| **S2 — Alto** | Funcionalidade não funciona como esperado, mas há workaround |
| **S3 — Médio** | Comportamento inconsistente, sem bloquear o uso |
| **S4 — Baixo** | Problema visual/cosmético, sem impacto funcional |

| Prioridade | Significado |
|---|---|
| **P0 — Urgente** | Bug crítico e reproduzível, com alto impacto |
| **P1 — Alta** | Impacta usuários de forma relevante |
| **P2 — Média** | Importante, mas pode esperar |
| **P3 — Baixa** | Backlog, sem prazo definido |

---

## 🧭 Como Navegar Neste Repositório

- Comece pelo [`documentacao/Plano_de_Testes.md`](./documentacao/Plano_de_Testes.md) para entender escopo e estratégia
- Veja os casos de teste em [`documentacao/Cenarios_e_Casos_de_Teste/`](./documentacao/Cenarios_e_Casos_de_Teste), organizados por funcionalidade
- Veja o resultado consolidado geral em [`documentacao/Resultado_dos_Testes.md`](./documentacao/Resultado_dos_Testes.md)
- Métricas detalhadas por módulo ficam em `metricas/`
- Bugs e melhorias encontrados durante a execução ficam documentados em `bug-reports/`, seguindo o template padrão
- Evidências (prints) referenciadas nos casos de teste e bugs ficam em `evidencias/`

---

## ⚖️ Disclaimer

Este projeto foi desenvolvido **exclusivamente para fins educacionais e de demonstração de habilidades em QA**.

Todos os testes foram realizados utilizando apenas funcionalidades públicas do site, sem exploração de vulnerabilidades, sem utilização de dados sensíveis e sem qualquer tentativa de comprometer a disponibilidade ou a segurança da aplicação.

Nenhuma compra foi concluída, nenhuma transação financeira foi realizada e nenhum dado pessoal de terceiros foi utilizado durante a execução dos testes.

A marca do site testado pertence aos seus respectivos proprietários. Este repositório não possui qualquer vínculo oficial com a empresa.

---

## 👨‍💻 Autor

**Miguel Luis**
Quality Assurance (QA) Júnior

- Testes Manuais
- Testes de API (Postman, Newman)
- Documentação de Testes
- Reporte de Bugs
- Planejamento de Testes
- ISTQB CTFL Certified

📎 LinkedIn: [linkedin.com/in/miguel-luisatf](https://www.linkedin.com/in/miguel-luisatf/)

---

> 🔎 **Nota final**
>
> O e-commerce testado neste projeto é o site da **Renner** (www.renner.com.br).
>
> Este repositório foi criado **exclusivamente com fins educacionais e de portfólio profissional**, como parte do processo de aprendizado e desenvolvimento prático de um QA júnior. Nenhuma parte deste projeto tem finalidade comercial: o autor **não obtém, e não busca obter, nenhum tipo de ganho financeiro** com esta documentação — seja por meio de venda, monetização, publicidade ou qualquer outra forma de retorno econômico.
>
> A escolha de um site real e público como objeto de estudo tem um propósito específico: simular, da forma mais realista possível, o dia a dia de um profissional de QA atuando sobre um produto de e-commerce em produção — algo que ambientes fictícios ou simulados nem sempre conseguem reproduzir com a mesma fidelidade. Testar um sistema real expõe o testador a nuances, comportamentos inesperados e casos de borda que dificilmente apareceriam em um cenário artificial, tornando o aprendizado mais completo e próximo da realidade do mercado.
>
> Todos os bugs e melhorias identificados durante a execução dos testes foram documentados com o mesmo rigor técnico que se espera em um ambiente profissional — não com o intuito de expor falhas ou prejudicar a imagem da marca, mas como um exercício genuíno de análise crítica e boas práticas de QA. Caso qualquer um dos achados aqui documentados seja, de alguma forma, útil para a equipe responsável pelo site identificar pontos de melhoria em sua plataforma, esse será um efeito colateral bem-vindo — mas em nenhum momento o objetivo principal do projeto, que permanece sendo o aprendizado e a construção de portfólio do autor.
>
> Reforça-se que:
> - Nenhuma vulnerabilidade de segurança foi explorada ou buscada intencionalmente;
> - Nenhum dado real de terceiros foi utilizado — todos os dados de teste (nomes, e-mails, CPFs, senhas, endereços) são fictícios;
> - Nenhuma compra foi finalizada e nenhuma transação financeira real foi realizada;
> - Este projeto não possui qualquer vínculo oficial, contratual ou institucional com a empresa proprietária do site testado;
> - Caso a empresa ou seus representantes tenham qualquer objeção quanto à existência deste material, o autor está aberto a rever, ajustar ou remover o conteúdo conforme solicitado.
>
> Em resumo: este é um projeto de estudo, feito por um profissional em início de carreira buscando demonstrar suas habilidades técnicas de forma ética e responsável — sem qualquer intenção comercial, maliciosa ou de exposição negativa da marca envolvida.
