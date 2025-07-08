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
