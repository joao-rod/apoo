<style>
    .ol {
        list-style-type: none;
        padding-left: 25px;
    }
</style>

# Casos de Uso

## UC01: Realizar Venda

### Ator(es):
* Cliente
* Operadora de pagamentos
* Funcionário

### Interessado(s) e interesse(s):

### Pré-condições:

### Pós-condições:

### Questões em aberto:

### Fluxo Principal:
1. O cliente escolhe os produtos e leva ao caixa.

2. [IN] O funcionário registra os itens.

3. [OUT] O sistema exibe o valor total da compra.

4. [IN] O funcionário finaliza a venda.

5. [OUT] O sistema informa as formas de pagamento.

6. [IN] O cliente escolhe a forma e realiza o pagamento.  
    6.1. Pagamento com dinheiro.  
    6.2. Pagamento com cartão de débito.  
    6.3. Pagamento com cartão de crédito.  
    6.4. Pagamento com Pix.  
    6.5. Pagamento com vale refeição.  

7. [OUT] O funcionário confirma o pagamento e entrega o comprovante ao cliente.

### Variantes
<ol class="ol">
  <li>
    <strong>6.1. Pagamento com dinheiro</strong>
    <ol class="ol">
      <li>6.1.1. O cliente entrega as notas.</li>
      <li>6.1.2. O funcionário registra o valor recebido.</li>
      <li>6.1.3. O sistema informa o troco.</li>
      <li>6.1.4. O funcionário entrega o troco ao cliente (se houver troco).</li>
    </ol>
  </li>
</ol>

<ol class="ol">
  <li>
    <strong>6.2. Pagamento com cartão de débito</strong>
    <ol class="ol">
      <li>6.2.1. O cliente usa o cartão na interface de identificação.</li>
      <li>6.2.2. O sistema envia os dados do cartão para a operadora de cartões.</li>
      <li>6.2.3. A operadora envia o número de autorização.</li>
    </ol>
  </li>
</ol>

<ol class="ol">
  <li>
    <strong>6.3. Pagamento com cartão de crédito</strong>
    <ol class="ol">
      <li>6.3.1. O cliente usa o cartão na interface de identificação.</li>
      <li>6.3.2. O sistema informa as opções de parcelamento.</li>
      <li>6.3.3. O cliente escolhe o parcelamento.</li>
      <li>6.3.4. O sistema envia os dados do cartão e parcelamento para a operadora de cartões.</li>
      <li>6.3.5 A operadora envia o número de autorização.</li>
    </ol>
  </li>
</ol>
  
<ol class="ol">
  <li>
    <strong>6.4. Pagamento com Pix</strong>
    <ol class="ol">
      <li>6.4.1. O sistema solicita uma chave para pagamento a operadora de <strong>pagamentos</strong></li>
      <li>6.4.2. O sistema exibe a chave para pagamento.</li>
      <li>6.4.3. O cliente realiza o pagamento.</li>
      <li>6.4.4. O operadora envia o número de autirização.</li>
      <li>6.4.5. O sistema registra o pagamento.</li>
    </ol>
  </li>
</ol>

<ol class="ol">
  <li>
    <strong>6.5. Pagamento com vale refeição</strong>
    <ol class="ol">
      <li>6.5.1. O cliente usa o cartão na interface de identificação.</li>
      <li>6.5.2. O sistema envia os dados do cartão para a operadora de cartões.</li>
      <li>6.5.3. A operadora envia o número de autorização.</li>
    </ol>
  </li>
</ol>

### Exceções
**Exceção 2a: Código de barras do produto ilegível**  
<ol class="ol">
    <li>2a.1 Funcionário solicita ao cliente para buscar outro produto.</li>
    <li>2a.2 [IN] Funcionário registra novamente o produto.</li>
</ol>
Avança para o passo 3.

<br>

**Exceção 2b: Funcionário registra quantidade incorreta de um produto**  
<ol class="ol">
    <li>2b.1 Funcionário solicita cancelamento da venda do produto.</li>
    <li>2b.2 [IN] Funcionário registra novamente o produto com a quantia correta.</li>
</ol>
Avança para o passo 4.

<br>

**Exceção 6.1.4a Troco insuficiente**  
<ol class="ol">
    <li>6.1.4a.1 O funcionário informa ao cliente.</li>
</ol>
Retorna ao passo 5.

<br>

**Exceção 6.2.2a A operadora não autoriza a compra**  
<ol class="ol">
    <li>6.2.2a.1 O funcionário informa ao cliente.</li>
</ol>
Retorna ao passo 5.

<br>

**Exceção 6.2.2a A operadora não autoriza a compra**  
<ol class="ol">
    <li>6.2.2a O funcionário informa ao cliente.</li>
</ol>
Retorna ao passo 5.  

<br>

**Exceção 6.4.3a Saldo insuficiente**  
<ol class="ol">
    <li>6.4.3a O funcionário informa ao cliente.</li>
</ol>
Retorna ao passo 5.  

<br>
