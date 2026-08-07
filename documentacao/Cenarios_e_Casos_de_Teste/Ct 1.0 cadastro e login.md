# 1.0 Cadastro e Login

**Módulo:** Cadastro e Login

**Aplicação:** Site do e-commerce testado (produção, terceiro)

**Tipo de teste:** Manual funcional

**Ambiente:** Produção (site público)

> ⚠️ Todos os dados utilizados nestes testes (nome, e-mail, telefone, senha) são fictícios. Nenhum dado pessoal real é inserido.

---

## CT-001 — Cadastro com dados válidos

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário não possui conta cadastrada / não está logado |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o site do e-commerce
2. Clicar em "Entrar" ou "Minha Conta"
3. Selecionar a opção de cadastro ("Criar conta" / "Cadastre-se")
4. Preencher todos os campos obrigatórios com dados fictícios válidos (nome, e-mail, senha, telefone, CPF de teste, data de nascimento)
5. Clicar em "Cadastrar" / "Continuar"

**Resultado esperado:**
A conta é criada com sucesso e o usuário é redirecionado para a área logada ou recebe uma mensagem de confirmação de cadastro.

---

## CT-002 — Cadastro com e-mail já existente

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Já existe uma conta cadastrada com o e-mail utilizado no teste |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a página de cadastro
2. Preencher o formulário utilizando um e-mail já cadastrado anteriormente
3. Clicar em "Cadastrar"

**Resultado esperado:**
O sistema exibe uma mensagem informando que o e-mail já está em uso e não permite a criação de uma conta duplicada.

---

## CT-003 — Cadastro com senha fora dos requisitos mínimos

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página de cadastro |
| **Prioridade** | Média |

**Passos:**
1. Acessar a página de cadastro
2. Preencher os demais campos corretamente
3. Inserir uma senha que não atenda aos requisitos mínimos (ex: menos de 6 caracteres, sem números)
4. Tentar enviar o formulário

**Resultado esperado:**
O sistema exibe uma mensagem indicando os requisitos de senha (quantidade mínima de caracteres, uso de números/letras, etc.) e não permite o envio até que a senha seja corrigida.

---

## CT-004 — Cadastro com campos obrigatórios vazios

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página de cadastro |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a página de cadastro
2. Deixar um ou mais campos obrigatórios em branco (ex: nome ou e-mail)
3. Clicar em "Cadastrar"

**Resultado esperado:**
O sistema destaca visualmente os campos obrigatórios não preenchidos e impede o envio do formulário.

---

## CT-005 — Cadastro com e-mail em formato inválido

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página de cadastro |
| **Prioridade** | Média |

**Passos:**
1. Acessar a página de cadastro
2. Preencher o campo de e-mail com um formato inválido (ex: "teste@@email", "testeemail.com")
3. Preencher os demais campos corretamente
4. Tentar enviar o formulário

**Resultado esperado:**
O sistema identifica o e-mail como inválido e exibe uma mensagem de erro, impedindo o envio do formulário.

---

## CT-006 — Cadastro com CPF inválido

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está na página de cadastro e o campo CPF é exigido |
| **Prioridade** | Média |

**Passos:**
1. Acessar a página de cadastro
2. Inserir um CPF com dígitos verificadores inválidos ou número incompleto
3. Preencher os demais campos corretamente
4. Tentar enviar o formulário

**Resultado esperado:**
O sistema valida o CPF e exibe mensagem de erro para CPF inválido, impedindo o cadastro.

---

## CT-007 — Login com credenciais válidas

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário já possui uma conta cadastrada (fictícia) |
| **Prioridade** | Alta |

**Passos:**
1. Acessar o site do e-commerce
2. Clicar em "Entrar"
3. Inserir e-mail e senha corretos
4. Clicar em "Entrar" / "Login"

**Resultado esperado:**
O usuário é autenticado com sucesso e passa a visualizar seu nome ou informações da conta na área logada.

---

## CT-008 — Login com senha incorreta

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário já possui uma conta cadastrada (fictícia) |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a tela de login
2. Inserir o e-mail correto e uma senha incorreta
3. Clicar em "Entrar"

**Resultado esperado:**
O sistema exibe uma mensagem de erro genérica (sem indicar especificamente se o erro foi no e-mail ou na senha, por questão de segurança) e não autentica o usuário.

---

## CT-009 — Login com e-mail não cadastrado

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Nenhuma (e-mail utilizado não deve existir na base) |
| **Prioridade** | Média |

**Passos:**
1. Acessar a tela de login
2. Inserir um e-mail que não possui cadastro
3. Inserir qualquer senha
4. Clicar em "Entrar"

**Resultado esperado:**
O sistema exibe mensagem de erro informando que as credenciais são inválidas, sem revelar se o e-mail existe ou não na base (boa prática de segurança).

---

## CT-010 — Recuperação de senha

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário possui conta cadastrada (fictícia) |
| **Prioridade** | Alta |

**Passos:**
1. Acessar a tela de login
2. Clicar em "Esqueci minha senha"
3. Informar o e-mail cadastrado
4. Confirmar a solicitação

**Resultado esperado:**
O sistema exibe uma mensagem confirmando que, caso o e-mail esteja cadastrado, um link/instrução de redefinição de senha foi enviado.

---

## CT-011 — Recuperação de senha com e-mail não cadastrado

| Campo | Detalhe |
|---|---|
| **Pré-condição** | E-mail informado não possui cadastro |
| **Prioridade** | Baixa |

**Passos:**
1. Acessar "Esqueci minha senha"
2. Informar um e-mail não cadastrado
3. Confirmar a solicitação

**Resultado esperado:**
O sistema não deve informar explicitamente se o e-mail existe ou não na base (boa prática de segurança); a mensagem exibida deve ser genérica.

---

## CT-012 — Persistência de sessão (login mantido)

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário realizou login com sucesso |
| **Prioridade** | Média |

**Passos:**
1. Realizar login na conta
2. Navegar por outras páginas do site
3. Fechar e reabrir a aba (sem fazer logout)

**Resultado esperado:**
O usuário permanece autenticado, sem necessidade de realizar login novamente (considerando comportamento padrão de sessão do site).

---

## CT-013 — Logout

| Campo | Detalhe |
|---|---|
| **Pré-condição** | Usuário está logado |
| **Prioridade** | Média |

**Passos:**
1. Estando logado, acessar o menu da conta
2. Clicar em "Sair" / "Logout"

**Resultado esperado:**
O usuário é deslogado com sucesso e redirecionado para a página inicial ou de login, sem mais acesso às informações da conta.

---

## Observações Gerais

- Todos os testes de cadastro devem utilizar dados fictícios criados especificamente para este projeto
- Nenhuma senha ou dado sensível real deve ser reutilizado de contas pessoais do testador
- Casos que dependerem de recebimento de e-mail (recuperação de senha) podem ser validados até o ponto de confirmação de envio, sem necessidade de acessar a caixa de entrada real
