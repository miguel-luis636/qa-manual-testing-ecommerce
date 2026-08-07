# Resultados de Execução — Módulo 1.0 Cadastro e Login

**Data da execução:** 21/07/2026

**Ambiente:** Google Chrome (última versão), Windows 11, Desktop

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Executor:** Miguel Luis

---

## 📊 Métricas do Módulo

| Métrica | Valor |
|---|---|
| Total de casos de teste planejados | 13 |
| Casos executados | 13 |
| Casos aprovados | 12 |
| Casos reprovados | 1 |
| Taxa de sucesso | 92,3% |
| Melhorias de usabilidade identificadas | 2 (MELHORIA-20260721-001, MELHORIA-20260721-002) |

---

## 📋 Resultado por Caso de Teste

| ID | Caso de Teste | Resultado | Observação |
|---|---|:---:|---|
| CT-001 | Cadastro com dados válidos | ✅ Passou | — |
| CT-002 | Cadastro com e-mail já existente | ✅ Passou | — |
| CT-003 | Cadastro com senha fora dos requisitos mínimos | ✅ Passou | — |
| CT-004 | Cadastro com campos obrigatórios vazios | ✅ Passou | — |
| CT-005 | Cadastro com e-mail em formato inválido | ✅ Passou | Mensagem de erro exibida, porém pouco clara sobre o que está incorreto (ver MELHORIA-20260721-001) |
| CT-006 | Cadastro com CPF inválido | ✅ Passou | — |
| CT-007 | Login com credenciais válidas | ✅ Passou | — |
| CT-008 | Login com senha incorreta | ✅ Passou | — |
| CT-009 | Login com e-mail não cadastrado | ✅ Passou | — |
| CT-010 | Recuperação de senha | ✅ Passou | — |
| CT-011 | Recuperação de senha com e-mail não cadastrado | ❌ **Não passou** | Sistema aceita CPF inexistente sem alertar o usuário (ver MELHORIA-20260721-002) |
| CT-012 | Persistência de sessão (login mantido) | ✅ Passou | — |
| CT-013 | Logout | ✅ Passou | — |

**Legenda:** ✅ Passou · ❌ Não passou · ⚠️ Passou com ressalva

---

## 💡 Melhorias de Usabilidade Identificadas Nesta Execução

| ID | Título | Prioridade Sugerida | Origem |
|---|---|---|---|
| MELHORIA-20260721-001 | Erro de "dado inválido" no cadastro sem indicar qual campo | Alta | CT-005 |
| MELHORIA-20260721-002 | Recuperação de senha sem feedback visual para dado inexistente | Média | CT-011 |

---

## 📝 Observações Gerais da Sessão

- Dados de teste utilizados (fictícios): CPF `709.446.182-86`, e-mail `maria.teste01@gmail.com`, nome `Maria Oliveira Santos`, senha `Qa#Test90`, telefone `21987654321`
- Após o envio do código de confirmação (etapa de verificação), **não há nenhuma confirmação visual clara de que o processo foi concluído com sucesso** — isso pode gerar confusão em parte dos usuários, que ficam sem saber se o cadastro/ação foi realmente finalizado. Esse ponto está registrado como observação de usabilidade e pode ser formalizado como uma nova sugestão de melhoria, caso se confirme em nova validação.
- Recomenda-se, em execução futura, capturar prints de cada etapa relevante (especialmente da mensagem de erro do CT-005 e do comportamento do CT-011) para anexar como evidência formal nas respectivas sugestões de melhoria.
