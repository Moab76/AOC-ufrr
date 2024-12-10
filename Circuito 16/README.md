# Decodificador 4-16 para Display de 7 Segmentos

Este circuito é um **decodificador de 4 bits** que converte uma entrada binária em um valor hexadecimal (de 0 a F) e exibe o valor correspondente em um **display de 7 segmentos** no Logisim.

![Decodificador](./Imagens/DECODIFICADOR.png)

[Link do circuito](./16-Decodificador-7-Seg-Hex.circ)

---

## Componentes do Circuito

1. **Decodificador 4-16**:
   - Converte a entrada de 4 bits (0000 a 1111) em 16 saídas individuais.
   - Cada saída é ativada para representar os números de 0 a F em hexadecimal.

2. **Lógica Combinacional**:
   - Usa as 16 saídas do decodificador para acionar as entradas de segmentos do display.
   - Define quais segmentos do display (a, b, c, d, e, f, g) devem ser ligados para representar cada dígito hexadecimal.

3. **Display de 7 Segmentos**:
   - Recebe os sinais lógicos e aciona os segmentos apropriados para exibir os caracteres 0 a F.

---

## Funcionamento

1. **Entrada**:
   - Um valor binário de 4 bits é inserido no circuito (por exemplo, `0000` para 0, `1111` para F).

2. **Decodificação**:
   - O decodificador 4-16 ativa uma única saída correspondente ao valor da entrada.
   - Exemplo:
     - Entrada: `0101` (5 em binário).
     - Saída do decodificador: ativa a linha 5.

3. **Lógica para Segmentos**:
   - As saídas do decodificador são conectadas a uma lógica combinacional que define os segmentos que devem ser ativados no display para cada valor.
   - Exemplo:
     - Para exibir "5", os segmentos **a, c, d, f, g** são ativados.

4. **Exibição**:
   - O display de 7 segmentos recebe os sinais e ilumina os segmentos necessários para formar o caractere correspondente.

---

## Tabela Verdade

Abaixo está a tabela verdade que define quais segmentos devem ser ativados para cada valor hexadecimal:

| Entrada (Binário) | Hexadecimal | a | b | c | d | e | f | g |
|--------------------|-------------|---|---|---|---|---|---|---|
| 0000               | 0           | 1 | 1 | 1 | 1 | 1 | 1 | 0 |
| 0001               | 1           | 0 | 1 | 1 | 0 | 0 | 0 | 0 |
| 0010               | 2           | 1 | 1 | 0 | 1 | 1 | 0 | 1 |
| 0011               | 3           | 1 | 1 | 1 | 1 | 0 | 0 | 1 |
| 0100               | 4           | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| 0101               | 5           | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
| 0110               | 6           | 1 | 0 | 1 | 1 | 1 | 1 | 1 |
| 0111               | 7           | 1 | 1 | 1 | 0 | 0 | 0 | 0 |
| 1000               | 8           | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 1001               | 9           | 1 | 1 | 1 | 1 | 0 | 1 | 1 |
| 1010               | A           | 1 | 1 | 1 | 0 | 1 | 1 | 1 |
| 1011               | B           | 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| 1100               | C           | 1 | 0 | 0 | 1 | 1 | 1 | 0 |
| 1101               | D           | 0 | 1 | 1 | 1 | 1 | 0 | 1 |
| 1110               | E           | 1 | 0 | 0 | 1 | 1 | 1 | 1 |
| 1111               | F           | 1 | 0 | 0 | 0 | 1 | 1 | 1 |

---

## Conclusão

Este circuito demonstra como combinar um **decodificador 4-16** com lógica combinacional e um display de 7 segmentos para exibir valores hexadecimais (0 a F). O uso do decodificador facilita a tradução direta da entrada binária para uma exibição visual, reduzindo a complexidade do circuito.
