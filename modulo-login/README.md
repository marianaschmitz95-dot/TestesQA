# Módulo de Login — SauceDemo

Documentação de testes funcionais do módulo de Login do site [SauceDemo](https://www.saucedemo.com/), cobrindo autenticação, validação de campos, controle de acesso e encerramento de sessão.

---

## Visão Geral

| Item              | Detalhe         |
|-------------------|-----------------|
| Site testado      | saucedemo.com   |
| Módulo            | Login           |
| Ciclo             | Login_1         |
| Build/Versão      | v1.0.1          |
| Ambiente          | QA              |
| Responsável       | Mariana         |
| Total de casos    | 8               |
| Passed            | 7               |
| Failed            | 1               |
| Taxa de sucesso   | 87,5%           |
| Bugs encontrados  | 1               |

---

## Casos de Teste

| Caso ID | Título | Prioridade | Resultado |
|---------|--------|------------|-----------|
| CT-001 | Login com credenciais válidas — standard_user | Alta | ✅ Passed |
| CT-002 | Login com senha incorreta | Alta | ✅ Passed |
| CT-003 | Login com ambos os campos em branco | Alta | ✅ Passed |
| CT-004 | Login apenas com username preenchido e senha em branco | Alta | ✅ Passed |
| CT-005 | Login com usuário bloqueado — locked_out_user | Alta | ✅ Passed |
| CT-006 | Login com usuário problem_user | Alta | ❌ Failed |
| CT-007 | Login com username inexistente no sistema | Alta | ✅ Passed |
| CT-008 | Logout após login bem-sucedido | Alta | ✅ Passed |

---

## Bug Encontrado

**BUG-001 — Página de inventário carrega com imagens incorretas após login com problem_user**

- Módulo: Login
- Severidade: Média
- Prioridade: Média
- Status: Em execução
- Caso relacionado: CT-006 / EXE-006

**Resumo:** Após autenticação bem-sucedida com o usuário `problem_user`, a página `/inventory.html` é carregada com imagens erradas em todos os produtos. Todos os itens exibem a mesma imagem, que não corresponde ao produto listado.

**Passos para reproduzir:**
1. Acessar https://www.saucedemo.com/
2. Preencher "Username" com `problem_user`
3. Preencher "Password" com `secret_sauce`
4. Clicar no botão "Login"
5. Observar as imagens exibidas na página de inventário

**Resultado atual:** Todos os produtos exibem a mesma imagem incorreta.  
**Resultado esperado:** Cada produto deve exibir sua imagem correspondente ao nome e descrição listados.  
**Evidência:** [CT-006-BUG-001.mp4](evidencias/CT-006-BUG-001.mp4)

---

## Evidências

As evidências em vídeo de cada caso de teste estão disponíveis na pasta `/evidencias`:

| Caso ID | Arquivo |
|---------|---------|
| CT-001 | [CT-001.mp4](evidencias/CT-001.mp4) |
| CT-002 | [CT-002.mp4](evidencias/CT-002.mp4) |
| CT-003 | [CT-003.mp4](evidencias/CT-003.mp4) |
| CT-004 | [CT-004.mp4](evidencias/CT-004.mp4) |
| CT-005 | [CT-005.mp4](evidencias/CT-005.mp4) |
| CT-006 | [CT-006-BUG-001.mp4](evidencias/CT-006-BUG-001.mp4) |
| CT-007 | [CT-007.mp4](evidencias/CT-007.mp4) |
| CT-008 | [CT-008.mp4](evidencias/CT-008.mp4) |

---

## Documentação Completa

A documentação detalhada dos casos de teste, execuções e bugs está disponível no arquivo:  
📄 [teste_login_saucedemo.xlsx](teste_login_saucedemo.xlsx)