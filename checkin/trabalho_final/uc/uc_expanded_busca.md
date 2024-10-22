# Caso de Uso: Busca por Marcações

**Ator(es):**
- Usuário

**Interessado(s) e interesse(s):**
- **Usuário:** Visualizar as marcações realizadas em um período.
- **Sistema:** Fornecer relatórios de registros em um período de tempo.

**Pré-condições:**
- O usuário deve ser registrado e estar logado no sistema.

**Pós-condições:**
- Não definidas.

**Questões em aberto:**
- A busca deve ser filtrada por data ou intervalo de tempo?
- O sistema permite exportação dos dados para outros formatos (ex.: PDF, Excel)?

**Fluxo Principal:**
1. [IN] O usuário seleciona a opção "Busca por Marcações" e define o período de busca.
2. [OUT] O sistema exibe as marcações do período solicitado.

**Variantes:**
- Não possui.

**Exceções:**
- **Exceção 1a:** O usuário define um período futuro (data futura).
  - 1a.1 [OUT] O sistema exibe uma mensagem de erro e busca pela última data de registros.
  - Avança ao passo 2.
