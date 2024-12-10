# Detector de Número Primo com Mapa de Karnaugh

Este projeto utiliza o **Logisim** para criar um circuito lógico que verifica se um número binário (de 4 bits) é primo. A lógica foi desenvolvida a partir da simplificação de expressões booleanas usando o **Mapa de Karnaugh**.

## Descrição do Circuito

### Entradas
O circuito possui 4 entradas binárias:  
- **A**, **B**, **C**, **D**, representando os bits do número em formato binário, com **A** sendo o bit mais significativo e **D** o menos significativo.

### Saída
- **S**: saída única que indica se o número é primo.  
  - **S = 1**: o número é primo.  
  - **S = 0**: o número **não** é primo.

### Função Lógica
- A saída **S** foi obtida a partir da análise dos números primos no intervalo representado por 4 bits (0 a 15).  
- Os números primos são: **2, 3, 5, 7, 11, 13**.  
- Representando estes números em binário:  
  - **2**: 0010  
  - **3**: 0011  
  - **5**: 0101  
  - **7**: 0111  
  - **11**: 1011  
  - **13**: 1101  

### Mapa de Karnaugh
O mapa de Karnaugh foi preenchido com **1** nas células correspondentes a números primos e **0** nos demais. A partir disso, a função lógica foi simplificada.

#### Função Simplificada
A expressão simplificada para **S** é:  
**S = A'BC'D + A'CD + BCD' + BC'D**

#### Função Completa (Sem Simplificação)
A expressão completa antes da simplificação é:  
**S = A'B'C'D + A'B'CD + A'BC'D + A'BCD + AB'C'D + AB'CD + ABC'D + ABCD**

### Implementação no Circuito
O circuito é composto por:  
- **Portas AND**: combinam as condições das expressões.  
- **Portas OR**: somam os resultados das expressões simplificadas.  
- As entradas são conectadas às portas de forma a respeitar a expressão lógica simplificada.

## Passo a Passo do Funcionamento
1. **Entrada dos valores**: Os 4 bits do número em binário são fornecidos como entrada.  
2. **Avaliação da lógica**: As portas lógicas avaliam as condições baseadas na expressão simplificada.  
3. **Resultado na saída**: Se o número for primo, a saída será **1**; caso contrário, será **0**.

## Benefícios da Simplificação
- Redução no número de portas lógicas necessárias.  
- Menor consumo de recursos no circuito.  
- Melhor desempenho e clareza na implementação.
    