# Circuito de Paridade Ímpar

Este circuito foi projetado para calcular a **paridade ímpar** de um conjunto de bits usando portas XOR no software Logisim. A verificação de paridade é uma técnica comum em sistemas digitais para detecção de erros em transmissões ou armazenamento de dados.

![Circuito de paridade imper](./Imagens/PARIDADEIMPAR.png)

[Link do circuito](./14-Paridade-Impar.circ)

---

## Objetivo do Circuito

O circuito de paridade ímpar determina se o número de bits `1` em um dado conjunto é **ímpar**. A saída do circuito será:

- **1**: Quando o número de bits `1` for ímpar.
- **0**: Quando o número de bits `1` for par.

---

## Componentes Principais

### 1. **Entradas**
   - Um barramento de entrada que aceita um conjunto de bits (neste caso, 8 bits).
   - Os bits podem ser configurados como `0` ou `1`.

### 2. **Portas XOR**
   - As portas XOR (ou exclusivas) são usadas para calcular a paridade.
   - A característica principal da porta XOR é que sua saída é `1` se, e somente se, o número de entradas `1` for ímpar.

### 3. **Saída**
   - Uma única saída representando o bit de paridade:
     - `1` para paridade ímpar.
     - `0` para paridade par.

---

## Funcionamento do Circuito

1. **Aplicação das Entradas**:
   - O barramento de 8 bits é alimentado com os valores a serem analisados.

2. **Processamento com Portas XOR**:
   - As portas XOR são organizadas de forma sequencial para calcular a paridade.
   - A cada estágio, duas entradas são processadas, e a saída resultante é usada na próxima etapa.

   Exemplo (4 bits simplificados):
   - Entrada: `1011`
   - XOR1: `1 XOR 0 = 1`
   - XOR2: `1 XOR 1 = 0`
   - XOR3: `0 XOR 1 = 1`
   - Saída: `1` (paridade ímpar).

3. **Resultado Final**:
   - A última porta XOR fornece o resultado final do cálculo da paridade.

---

## Características do Circuito

- **Escalabilidade**:
  - O número de bits pode ser aumentado ou reduzido conforme necessário, adicionando ou removendo portas XOR.

- **Baixa Latência**:
  - O tempo de processamento depende apenas do número de níveis de portas XOR, que cresce logaritmicamente com o número de bits.

- **Simplicidade**:
  - O uso exclusivo de portas XOR torna o circuito fácil de implementar e otimizado para hardware digital.

---

## Aplicações

1. **Detecção de Erros**:
   - Utilizado em sistemas de comunicação para verificar a integridade dos dados transmitidos.

2. **Codificação de Dados**:
   - Implementado em códigos de detecção e correção de erros (ex.: código de Hamming).

3. **Redundância**:
   - Garantia de redundância em protocolos de dados digitais.

---

## Possíveis Extensões

1. **Paridade Par**:
   - O circuito pode ser adaptado para calcular a paridade par, invertendo a lógica da saída.

2. **Barramentos Maiores**:
   - Expansão para processar barramentos de 16, 32 ou 64 bits.

3. **Visualização**:
   - Adicionar LEDs ou displays para visualizar as entradas e a saída do circuito.

---

Este circuito demonstra a aplicação prática de portas XOR para verificar a paridade ímpar em sistemas digitais, um conceito fundamental para a confiabilidade em eletrônica e computação.
