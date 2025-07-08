Para resolver este problema, vou usar as leis de Kirchhoff e a Lei de Ohm.

**Problema 2.18:** Dado o circuito mostrado na Figura P2.18, determine:
a) o valor de $i_a$
b) o valor de $i_b$
c) o valor de $v_o$
d) a potência dissipada em cada resistor
e) a potência fornecida pela fonte de 50 V

**Solução:**

Primeiro, vamos identificar os nós e as correntes no circuito. Temos um circuito em série-paralelo.

Podemos usar a Lei das Correntes de Kirchhoff (LCK) e a Lei das Tensões de Kirchhoff (LTK).

Vamos começar simplificando o circuito. Os resistores de 20 Ω e 80 Ω estão em paralelo.
A resistência equivalente ($R_{eq}$) desses dois resistores é:
$R_{eq} = \frac{20 \Omega \times 80 \Omega}{20 \Omega + 80 \Omega} = \frac{1600}{100} = 16 \Omega$

Agora, o circuito se torna uma fonte de tensão de 50 V em série com um resistor de 4 Ω e a resistência equivalente de 16 Ω.

A corrente total ($I_{total}$) que sai da fonte de 50 V é:
$I_{total} = \frac{50 V}{4 \Omega + 16 \Omega} = \frac{50 V}{20 \Omega} = 2.5 A$

Agora, vamos determinar os valores solicitados:

**a) o valor de $i_a$**
A corrente $i_a$ é a corrente que passa pelo resistor de 20 Ω. Podemos usar o divisor de corrente. A corrente total que entra no paralelo de 20 Ω e 80 Ω é $I_{total} = 2.5 A$.
$i_a = I_{total} \times \frac{80 \Omega}{20 \Omega + 80 \Omega} = 2.5 A \times \frac{80}{100} = 2.5 A \times 0.8 = 2 A$
Portanto, $i_a = 2 A$.

**b) o valor de $i_b$**
A corrente $i_b$ é a corrente que passa pelo resistor de 80 Ω.
$i_b = I_{total} \times \frac{20 \Omega}{20 \Omega + 80 \Omega} = 2.5 A \times \frac{20}{100} = 2.5 A \times 0.2 = 0.5 A$
Podemos verificar usando a LCK no nó superior do paralelo: $I_{total} = i_a + i_b \Rightarrow 2.5 A = 2 A + 0.5 A$, o que está correto.
Portanto, $i_b = 0.5 A$.

**c) o valor de $v_o$**
A tensão $v_o$ é a tensão no resistor de 80 Ω. Como os resistores de 20 Ω e 80 Ω estão em paralelo, a tensão em ambos é a mesma.
$v_o = i_b \times 80 \Omega = 0.5 A \times 80 \Omega = 40 V$
Ou, usando $i_a$:
$v_o = i_a \times 20 \Omega = 2 A \times 20 \Omega = 40 V$
Portanto, $v_o = 40 V$.

**d) a potência dissipada em cada resistor**
A potência dissipada em um resistor pode ser calculada por $P = I^2R$ ou $P = \frac{V^2}{R}$.

*   **Resistor de 4 Ω:**
    A corrente que passa por ele é $I_{total} = 2.5 A$.
    $P_{4\Omega} = (2.5 A)^2 \times 4 \Omega = 6.25 \times 4 = 25 W$

*   **Resistor de 20 Ω:**
    A corrente que passa por ele é $i_a = 2 A$.
    $P_{20\Omega} = (2 A)^2 \times 20 \Omega = 4 \times 20 = 80 W$
    Ou, usando a tensão $v_o = 40 V$:
    $P_{20\Omega} = \frac{(40 V)^2}{20 \Omega} = \frac{1600}{20} = 80 W$

*   **Resistor de 80 Ω:**
    A corrente que passa por ele é $i_b = 0.5 A$.
    $P_{80\Omega} = (0.5 A)^2 \times 80 \Omega = 0.25 \times 80 = 20 W$
    Ou, usando a tensão $v_o = 40 V$:
    $P_{80\Omega} = \frac{(40 V)^2}{80 \Omega} = \frac{1600}{80} = 20 W$

**e) a potência fornecida pela fonte de 50 V**
A potência fornecida pela fonte é $P_{fonte} = V_{fonte} \times I_{total}$.
$P_{fonte} = 50 V \times 2.5 A = 125 W$

**Verificação (Potência total dissipada vs. Potência total fornecida):**
A soma das potências dissipadas nos resistores deve ser igual à potência fornecida pela fonte.
$P_{total\_dissipada} = P_{4\Omega} + P_{20\Omega} + P_{80\Omega} = 25 W + 80 W + 20 W = 125 W$
Como $P_{total\_dissipada} = 125 W$ e $P_{fonte} = 125 W$, a solução está consistente.

**Respostas:**
a) $i_a = 2 A$
b) $i_b = 0.5 A$
c) $v_o = 40 V$
d) $P_{4\Omega} = 25 W$, $P_{20\Omega} = 80 W$, $P_{80\Omega} = 20 W$
e) $P_{fonte} = 125 W$



**Problema 2.23:** O resistor variável R no circuito da Figura P2.23 é ajustado até que $i_o$ seja igual a 10 mA. Determine o valor de R.

**Solução:**

Vamos usar a Lei de Ohm e as Leis de Kirchhoff para resolver este problema.

Primeiro, vamos converter os valores de resistência de kΩ para Ω:
1.5 kΩ = 1500 Ω
3 kΩ = 3000 Ω
5 kΩ = 5000 Ω

Sabemos que $i_o = 10 mA = 0.01 A$.
A corrente $i_o$ passa pelo resistor de 5 kΩ. Podemos encontrar a tensão através do resistor de 5 kΩ (vamos chamar de $V_{5k\Omega}$):
$V_{5k\Omega} = i_o \times 5000 \Omega = 0.01 A \times 5000 \Omega = 50 V$

Agora, vamos analisar o nó onde o resistor de 5 kΩ está conectado (o nó central, vamos chamá-lo de Nó A). A tensão neste nó em relação ao terra (parte inferior do circuito) é de 50 V.

Vamos chamar o nó entre o resistor de 3 kΩ e 500 Ω de Nó B.

Se considerarmos o nó inferior como referência (0 V):
*   A tensão no nó à esquerda da fonte de 80 V é 0 V.
*   A tensão no nó à direita da fonte de 80 V (Nó da fonte) é 80 V.

Sabemos que a corrente $i_o$ (10 mA) flui para baixo através do resistor de 5 kΩ.
A tensão no Nó A ($V_A$) é $i_o \times 5000 \Omega = 0.01 A \times 5000 \Omega = 50 V$.

Agora, vamos aplicar a LCK no Nó A:
Corrente entrando no Nó A = Corrente saindo do Nó A
A corrente que entra no Nó A vem do resistor de 1.5 kΩ.
A corrente que sai do Nó A vai para o resistor de 5 kΩ ($i_o$) e para o resistor de 3 kΩ.

$\frac{80 V - V_A}{1500 \Omega} = i_o + \frac{V_A - V_B}{3000 \Omega}$
$\frac{80 V - 50 V}{1500 \Omega} = 0.01 A + \frac{50 V - V_B}{3000 \Omega}$
$\frac{30 V}{1500 \Omega} = 0.01 A + \frac{50 V - V_B}{3000 \Omega}$
$0.02 A = 0.01 A + \frac{50 V - V_B}{3000 \Omega}$
$0.01 A = \frac{50 V - V_B}{3000 \Omega}$
$0.01 A \times 3000 \Omega = 50 V - V_B$
$30 V = 50 V - V_B$
$V_B = 50 V - 30 V = 20 V$

Agora que temos $V_B = 20 V$, podemos analisar o ramo do resistor de 500 Ω e o resistor variável R.
A tensão no resistor de 500 Ω é $V_B = 20 V$.
A corrente através do resistor de 500 Ω ($i_{500\Omega}$) é:
$i_{500\Omega} = \frac{V_B}{500 \Omega} = \frac{20 V}{500 \Omega} = 0.04 A = 40 mA$

Agora, vamos aplicar a LCK no Nó B. As correntes que saem do Nó B são:
1.  Corrente através do resistor de 500 Ω ($i_{500\Omega}$).
2.  Corrente através do resistor variável R (vamos chamar de $i_R$).

A corrente que entra no Nó B é a corrente que vem do resistor de 3 kΩ, que é $\frac{V_A - V_B}{3000 \Omega}$.
$\frac{50 V - 20 V}{3000 \Omega} = \frac{30 V}{3000 \Omega} = 0.01 A = 10 mA$

Então, aplicando a LCK no Nó B:
Corrente entrando no Nó B = Corrente saindo do Nó B
$0.01 A = i_{500\Omega} + i_R$
$0.01 A = 0.04 A + i_R$
$i_R = 0.01 A - 0.04 A = -0.03 A = -30 mA$

O sinal negativo para $i_R$ significa que a corrente está fluindo na direção oposta à que foi implicitamente assumida (ou seja, está fluindo do Nó B para o Nó da fonte, ou seja, para cima no diagrama).

A tensão através de R é a diferença de potencial entre o nó superior (Nó da fonte, 80 V) e o Nó B (20 V).
$V_R = 80 V - V_B = 80 V - 20 V = 60 V$

Agora, podemos calcular o valor de R usando a Lei de Ohm:
$R = \frac{V_R}{|i_R|}$ (usamos o valor absoluto da corrente, pois a resistência é sempre positiva)
$R = \frac{60 V}{0.03 A} = 2000 \Omega = 2 k\Omega$

**Respostas:**
O valor de R é $2 k\Omega$.
