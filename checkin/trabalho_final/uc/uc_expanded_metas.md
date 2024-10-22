# Caso de Uso: Define Metas

**Ator(es):**
- Usuário

**Interessado(s) e interesse(s):**
- **Usuário:** Configurar metas de horas trabalhadas por dia, semana ou mês.
- **Sistema:** Armazenar as metas e fornecer feedback quando forem atingidas.

**Pré-condições:**
- O usuário deve ser registrado e estar logado no sistema.

**Pós-condições:**
- As metas devem ser salvas no sistema para serem utilizadas no controle de tempo.

**Questões em aberto:**
- O sistema irá notificar o usuário via email ao atingir as metas?

**Fluxo Principal:**
1. [IN] O usuário seleciona a opção “Configurar Metas”.
2. [OUT] O sistema exibe a configuração atual e permite ajustes.
3. [IN] O usuário escolhe o tipo de meta (diária, semanal ou mensal) e define sua meta de horas.
4. [OUT] O sistema armazena as metas definidas.

**Variantes:**
- Não possui.

**Exceções:**
- **Exceção 4a:** O usuário define uma meta inválida.
  - 4a.1 [OUT] O sistema exibe uma mensagem de erro.
  - Retorna ao passo 2.
