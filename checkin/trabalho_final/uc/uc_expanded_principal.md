# Caso de Uso: Realiza Marcações

**Ator(es):**
- Usuário

**Interessado(s) e interesse(s):**
- **Usuário:** Registra os horários de entrada e saída para controle das horas trabalhadas.
- **Sistema:** Registra as marcações e calcula as horas de trabalho automaticamente.

**Pré-condições:**
- O usuário deve ser registrado e estar logado no sistema.

**Pós-condições:**
- Se for uma marcação de saída, o sistema recalcula automaticamente as horas trabalhadas até o momento.

**Questões em aberto:**
- O sistema precisa lidar com fusos horários ou ajustes de horário de verão?

**Fluxo Principal:**
1. [IN] O usuário acessa a funcionalidade "Realizar marcação".
2. [OUT] O sistema identifica o tipo de marcação e exibe a hora atual para o usuário.
   - **2.1. Variante:** Entrada
   - **2.2. Variante:** Saída
3. [IN] O usuário confirma a marcação.
4. [OUT] O sistema registra o horário de entrada/saída e, se a marcação for uma saída, recalcula e exibe as horas trabalhadas no dia atual.

**Variantes:**
- **2.1 Entrada**
  - 2.1.1 [OUT] O sistema verifica se o número de marcações do dia é ímpar, e se for, define que a marcação é uma entrada.
- **2.2 Saída**
  - 2.2.1 [OUT] O sistema verifica se o número de marcações do dia é par, e se for, define que a marcação é uma saída.

**Exceções:**
- Não possui.
