# Problema 2.18:
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
Como $P_{total\_dissipada} = 125 W$ e $P_{fonte} = 125 W$.

**Respostas:**
a) $i_a = 2 A$
b) $i_b = 0.5 A$
c) $v_o = 40 V$
d) $P_{4\Omega} = 25 W$, $P_{20\Omega} = 80 W$, $P_{80\Omega} = 20 W$
e) $P_{fonte} = 125 W$



# Problema 2.23:

**Solução:**

Primeiro, converter os valores de resistência de kΩ para Ω:
1.5 kΩ = 1500 Ω
3 kΩ = 3000 Ω
5 kΩ = 5000 Ω

Sabendo que $i_o = 10 mA = 0.01 A$.
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


# Problema 2.24:

**Solução usando Análise de Malhas**

**Interpretação das Malhas e Corrente de 4 A:**
As equações de malha são:
1.  $(10 + R)i_1 - Ri_2 - 10i_3 = 240$
2.  $-Ri_1 + (19 + R)i_2 - 4i_3 = 0$
3.  $-10i_1 - 4i_2 + 34i_3 = 0$

A corrente de 4 A no diagrama está localizada no ramo superior, que contém os resistores de 5 Ω e 10 Ω. Com base na estrutura das equações fornecidas, a corrente $i_2$ é a corrente de malha que passa por esses resistores. Portanto, assumimos que:
$i_2 = 4 A$

**a) Determine R:**

Substituímos $i_2 = 4 A$ nas três equações:

**Equação 1:**
$(10 + R)i_1 - R(4) - 10i_3 = 240$
$(10 + R)i_1 - 10i_3 = 240 + 4R$ (Equação 1')

**Equação 2:**
$-Ri_1 + (19 + R)(4) - 4i_3 = 0$
$-Ri_1 + 76 + 4R - 4i_3 = 0$
$-Ri_1 - 4i_3 = -76 - 4R$ (Equação 2')

**Equação 3:**
$-10i_1 - 4(4) + 34i_3 = 0$
$-10i_1 - 16 + 34i_3 = 0$
$-10i_1 + 34i_3 = 16$ (Equação 3')

Agora, temos um sistema de três equações com duas incógnitas ($i_1, i_3$) e o valor de R a ser determinado.

Da Equação 3', podemos expressar $i_1$ em termos de $i_3$:
$-10i_1 = 16 - 34i_3$
$i_1 = \frac{16 - 34i_3}{-10} = \frac{34i_3 - 16}{10} = \frac{17i_3 - 8}{5}$

Substituímos esta expressão para $i_1$ na Equação 1':
$(10 + R)\left(\frac{17i_3 - 8}{5}\right) - 10i_3 = 240 + 4R$
Multiplicamos toda a equação por 5 para eliminar o denominador:
$(10 + R)(17i_3 - 8) - 50i_3 = 5(240 + 4R)$
$170i_3 - 80 + 17Ri_3 - 8R - 50i_3 = 1200 + 20R$
Agrupamos os termos com $i_3$:
$(170 + 17R - 50)i_3 = 1200 + 20R + 80 + 8R$
$(120 + 17R)i_3 = 1280 + 28R$
$i_3 = \frac{1280 + 28R}{120 + 17R}$ (Equação 4')

Agora, substituímos a expressão para $i_1$ na Equação 2':
$-R\left(\frac{17i_3 - 8}{5}\right) - 4i_3 = -76 - 4R$
Multiplicamos toda a equação por 5 para eliminar o denominador:
$-R(17i_3 - 8) - 20i_3 = 5(-76 - 4R)$
$-17Ri_3 + 8R - 20i_3 = -380 - 20R$
Agrupamos os termos com $i_3$:
$(-17R - 20)i_3 = -380 - 20R - 8R$
$(-17R - 20)i_3 = -380 - 28R$
$(17R + 20)i_3 = 380 + 28R$
$i_3 = \frac{380 + 28R}{17R + 20}$ (Equação 5')

Agora, igualamos as Equações 4' e 5' para resolver para R:
$\frac{1280 + 28R}{120 + 17R} = \frac{380 + 28R}{17R + 20}$
Multiplicamos cruzado:
$(1280 + 28R)(17R + 20) = (380 + 28R)(120 + 17R)$

Expandimos ambos os lados:
Lado Esquerdo:
$1280 \times 17R + 1280 \times 20 + 28R \times 17R + 28R \times 20$
$21760R + 25600 + 476R^2 + 560R$
$476R^2 + 22320R + 25600$

Lado Direito:
$380 \times 120 + 380 \times 17R + 28R \times 120 + 28R \times 17R$
$45600 + 6460R + 3360R + 476R^2$
$476R^2 + 9820R + 45600$

Igualamos os lados:
$476R^2 + 22320R + 25600 = 476R^2 + 9820R + 45600$

Os termos $476R^2$ se cancelam:
$22320R + 25600 = 9820R + 45600$
$22320R - 9820R = 45600 - 25600$
$12500R = 20000$
$R = \frac{20000}{12500} = \frac{200}{125} = \frac{8}{5}$
$R = 1.6 \Omega$

**b) Potência fornecida pela fonte de 240 V:**

Para calcular a potência fornecida pela fonte, precisamos da corrente $i_1$.
Com $R = 1.6 \Omega$, calculamos $i_3$ usando a Equação 5':
$i_3 = \frac{380 + 28(1.6)}{17(1.6) + 20} = \frac{380 + 44.8}{27.2 + 20} = \frac{424.8}{47.2} = 9 A$

Agora, calculamos $i_1$ usando a expressão $i_1 = \frac{17i_3 - 8}{5}$:
$i_1 = \frac{17(9) - 8}{5} = \frac{153 - 8}{5} = \frac{145}{5} = 29 A$

A corrente que sai da fonte de 240 V é $i_1$.
$P_{fonte} = V_{fonte} \times i_1 = 240 V \times 29 A = 6960 W$

**Respostas:**
a) $R = 1.6 \Omega$
b) $P_{fonte} = 6960 W$


# Problema 2.25:
a) Determine a potência dissipada em cada resistor.
b) Determine a potência fornecida pela fonte ideal de tensão de 125 V.
c) Verifique que a potência fornecida é igual à potência total dissipada.

**Solução:**

**1. Determinação das Correntes de Malha:**

Com base nas equações de malha fornecidas e no diagrama do circuito, as correntes de malha $i_1$, $i_2$ e $i_3$ são definidas no sentido horário.

A informação chave é que a tensão no resistor de 16 Ω é 80 V, positiva no terminal superior. Isso significa que a corrente que flui através do resistor de 16 Ω é de cima para baixo. No diagrama, a corrente de malha $i_3$ é a única corrente que passa por este resistor e flui no sentido indicado.
Portanto, podemos determinar $i_3$ usando a Lei de Ohm:
$i_3 = \frac{V_{16\Omega}}{R_{16\Omega}} = \frac{80 V}{16 \Omega} = 5 A$

Agora, utilizamos o sistema de equações de malha fornecido, substituindo $i_3 = 5 A$:

**Equações de Malha (com $i_3 = 5 A$):**

*   **Malha 1:**
    $37i_1 - 7i_2 - 30i_3 = 125$
    $37i_1 - 7i_2 - 30(5) = 125$
    $37i_1 - 7i_2 - 150 = 125$
    $37i_1 - 7i_2 = 275$ (Equação A')

*   **Malha 2:**
    $-7i_1 + 27i_2 - 5i_3 = 0$
    $-7i_1 + 27i_2 - 5(5) = 0$
    $-7i_1 + 27i_2 - 25 = 0$
    $-7i_1 + 27i_2 = 25$ (Equação B')

*   **Malha 3:**
    $-30i_1 - 5i_2 + 51i_3 = 0$
    $-30i_1 - 5i_2 + 51(5) = 0$
    $-30i_1 - 5i_2 + 255 = 0$
    $-30i_1 - 5i_2 = -255$
    $30i_1 + 5i_2 = 255$ (Equação C')

Agora, resolvemos o sistema de equações lineares para $i_1$ e $i_2$ usando as Equações A' e B':

Multiplicamos a Equação A' por 27 e a Equação B' por 7 para eliminar $i_2$:
$(37i_1 - 7i_2 = 275) \times 27 \implies 999i_1 - 189i_2 = 7425$
$(-7i_1 + 27i_2 = 25) \times 7 \implies -49i_1 + 189i_2 = 175$

Somamos as duas novas equações:
$(999i_1 - 189i_2) + (-49i_1 + 189i_2) = 7425 + 175$
$950i_1 = 7600$
$i_1 = \frac{7600}{950} = 8 A$

Substituímos $i_1 = 8 A$ na Equação B' para encontrar $i_2$:
$-7(8) + 27i_2 = 25$
$-56 + 27i_2 = 25$
$27i_2 = 81$
$i_2 = \frac{81}{27} = 3 A$

Para verificar a consistência, substituímos $i_1 = 8 A$ e $i_2 = 3 A$ na Equação C':
$30(8) + 5(3) = 255$
$240 + 15 = 255$
$255 = 255$
A consistência é confirmada.

As correntes de malha são:
$i_1 = 8 A$
$i_2 = 3 A$
$i_3 = 5 A$

**a) Determine a potência dissipada em cada resistor.**
A potência dissipada em um resistor é calculada por $P = I_{ramo}^2 R$.

*   **Resistor de 7 Ω:**
    Corrente no ramo: $I_{7\Omega} = i_1 - i_2 = 8 A - 3 A = 5 A$.
    $P_{7\Omega} = (5 A)^2 \times 7 \Omega = 25 \times 7 = 175 W$.

*   **Resistor de 15 Ω:**
    Corrente no ramo: $I_{15\Omega} = i_2 = 3 A$.
    $P_{15\Omega} = (3 A)^2 \times 15 \Omega = 9 \times 15 = 135 W$.

*   **Resistor de 5 Ω:**
    Corrente no ramo: $I_{5\Omega} = i_2 - i_3 = 3 A - 5 A = -2 A$. (A magnitude da corrente é 2 A).
    $P_{5\Omega} = (-2 A)^2 \times 5 \Omega = 4 \times 5 = 20 W$.

*   **Resistor de 30 Ω:**
    Corrente no ramo: $I_{30\Omega} = i_1 - i_3 = 8 A - 5 A = 3 A$.
    $P_{30\Omega} = (3 A)^2 \times 30 \Omega = 9 \times 30 = 270 W$.

*   **Resistor de 16 Ω:**
    Corrente no ramo: $I_{16\Omega} = i_3 = 5 A$.
    $P_{16\Omega} = (5 A)^2 \times 16 \Omega = 25 \times 16 = 400 W$.
    (Alternativamente, $P_{16\Omega} = \frac{V_{16\Omega}^2}{R_{16\Omega}} = \frac{(80 V)^2}{16 \Omega} = \frac{6400}{16} = 400 W$).

**b) Determine a potência fornecida pela fonte ideal de tensão de 125 V.**
A potência fornecida por uma fonte de tensão é $P_{fonte} = V_{fonte} \times I_{fonte}$.
A corrente que sai do terminal positivo da fonte de 125 V é a corrente de malha $i_1$.
$P_{fonte} = 125 V \times i_1 = 125 V \times 8 A = 1000 W$.

**c) Verifique que a potência fornecida é igual à potência total dissipada.**
Calculamos a potência total dissipada somando as potências dissipadas em cada resistor:
$P_{total\_dissipada} = P_{7\Omega} + P_{15\Omega} + P_{5\Omega} + P_{30\Omega} + P_{16\Omega}$
$P_{total\_dissipada} = 175 W + 135 W + 20 W + 270 W + 400 W = 1000 W$.

A potência total fornecida (1000 W) é igual à potência total dissipada (1000 W), o que confirma a correção da solução.

**Respostas:**
a) $P_{7\Omega} = 175 W$, $P_{15\Omega} = 135 W$, $P_{5\Omega} = 20 W$, $P_{30\Omega} = 270 W$, $P_{16\Omega} = 400 W$.
b) $P_{fonte} = 1000 W$.
c) A potência fornecida (1000 W) é igual à potência total dissipada (1000 W).



# Problema 2.26:
a) Determine $i_a$.
b) Determine a potência dissipada em cada resistor.
c) Determine $v_o$.
d) Mostre que a potência fornecida pela fonte de corrente é igual à potência absorvida por todos os outros elementos.

**Assunções e Variáveis:**
*   $i_b = -2 A$ (corrente no ramo de 11 Ω, da esquerda para a direita).
*   $i_a = 4 A$ (corrente no ramo de 15 Ω, da esquerda para a direita).
*   $i_g$ é a corrente da fonte de corrente (para baixo).
*   $i_3$ é a corrente que passa pelos resistores de 4 Ω e 16 Ω.
*   $i_2$ é a corrente que passa pelo resistor de 30 Ω.
*   $i_1$ é a corrente que passa pelo resistor de 5 Ω.
*   $v_g$ é a tensão na fonte de corrente.
*   A equação (1) é uma relação de Kirchhoff: $100 + 30 \cdot i_b - 20 \cdot i_3 + 15 \cdot i_a = 0$.
*   A LCK no "ponto d" (nó inferior da fonte de corrente) é: $i_g + i_3 + i_a = 0$.
*   A LCK no "ponto b" (nó superior direito) é: $i_2 - i_b - i_3 = 0$.
*   A LCK no "ponto c" (nó superior esquerdo) é: $i_1 - i_g - i_2 = 0$.

---

**Passo 1: Determinar correntes $i_a, i_3, i_g, i_2, i_1$.**

**a) Determine $i_a$.**
$i_a$ é dado como 4 A.
$i_a = 4 A$.

**Cálculo de $i_3$:**
Usamos a equação (1):
$100 + 30 \cdot i_b - 20 \cdot i_3 + 15 \cdot i_a = 0$
Substituímos $i_b = -2 A$ e $i_a = 4 A$:
$100 + 30(-2) - 20i_3 + 15(4) = 0$
$100 - 60 - 20i_3 + 60 = 0$
$100 - 20i_3 = 0$
$20i_3 = 100$
$i_3 = 5 A$.

**Cálculo de $i_g$:**
Aplicando a LCK no "ponto d" (nó inferior da fonte de corrente):
$i_g + i_3 + i_a = 0$
$i_g = -i_3 - i_a$
$i_g = -5 A - 4 A$
$i_g = -9 A$.

**Cálculo de $i_2$:**
Aplicando a LCK no "ponto b" (nó superior direito, entre 11 Ω, 30 Ω e 10 Ω):
$i_2 - i_b - i_3 = 0$
$i_2 = i_b + i_3$
$i_2 = -2 A + 5 A$
$i_2 = 3 A$.

**Cálculo de $i_1$:**
Aplicando a LCK no "ponto c" (nó superior esquerdo, entre 9 Ω, 5 Ω e $i_g$):
$i_1 - i_g - i_2 = 0$
$i_1 = i_g + i_2$
$i_1 = -9 A + 3 A$
$i_1 = -6 A$.

---

**b) Determine a potência dissipada em cada resistor.**
Usamos $P = I^2 R$.

*   **Resistor de 9 Ω:**
    $P_{9\Omega} = (i_b)^2 \times 9 \Omega = (-2 A)^2 \times 9 \Omega = 4 \times 9 = 36 W$.

*   **Resistor de 11 Ω:**
    $P_{11\Omega} = (i_b)^2 \times 11 \Omega = (-2 A)^2 \times 11 \Omega = 4 \times 11 = 44 W$.

*   **Resistor de 10 Ω:**
    $P_{10\Omega} = (i_b)^2 \times 10 \Omega = (-2 A)^2 \times 10 \Omega = 4 \times 10 = 40 W$.

*   **Resistor de 5 Ω:**
    $P_{5\Omega} = (i_1)^2 \times 5 \Omega = (-6 A)^2 \times 5 \Omega = 36 \times 5 = 180 W$.

*   **Resistor de 30 Ω:**
    $P_{30\Omega} = (i_2)^2 \times 30 \Omega = (3 A)^2 \times 30 \Omega = 9 \times 30 = 270 W$.

*   **Resistor de 4 Ω:**
    $P_{4\Omega} = (i_3)^2 \times 4 \Omega = (5 A)^2 \times 4 \Omega = 25 \times 4 = 100 W$.

*   **Resistor de 16 Ω:**
    $P_{16\Omega} = (i_3)^2 \times 16 \Omega = (5 A)^2 \times 16 \Omega = 25 \times 16 = 400 W$.

*   **Resistor de 15 Ω:**
    $P_{15\Omega} = (i_a)^2 \times 15 \Omega = (4 A)^2 \times 15 \Omega = 16 \times 15 = 240 W$.

---

**c) Determine $v_o$.**
Assumindo que $v_o$ no enunciado se refere a $v_g$ (tensão na fonte de corrente).
Equação $v_g - 30i_2 - 4i_3 - 16i_3 = 0$.
$v_g = 30i_2 + 4i_3 + 16i_3$
$v_g = 30i_2 + 20i_3$
Substituímos $i_2 = 3 A$ e $i_3 = 5 A$:
$v_g = 30(3) + 20(5)$
$v_g = 90 + 100$
$v_g = 190 V$.

---

**d) Mostre que a potência fornecida pela fonte de corrente é igual à potência absorvida por todos os outros elementos.**

**Potência fornecida pela fonte de corrente ($P_g$):**
$P_g = i_g v_g$
$P_g = (-9 A)(190 V) = -1710 W$.
O sinal negativo indica que a fonte de corrente está absorvendo 1710 W. Portanto, ela **fornece** 1710 W.

**Potência absorvida por todos os outros elementos:**
O material inclui a potência da fonte de 100 V como absorvida em 400 W.
$P_{absorvida} = P_{9\Omega} + P_{11\Omega} + P_{10\Omega} + P_{5\Omega} + P_{30\Omega} + P_{4\Omega} + P_{16\Omega} + P_{15\Omega} + P_{fonte\_100V\_absorvida}$
$P_{absorvida} = 36 W + 44 W + 40 W + 180 W + 270 W + 100 W + 400 W + 240 W + 400 W$
$P_{absorvida} = 1710 W$.

A potência fornecida pela fonte de corrente (1710 W) é igual à potência absorvida por todos os outros elementos (1710 W), o que verifica o balanço de potência.

**Respostas Finais:**

**a) $i_a = 4 A$.**

**b) Potência dissipada em cada resistor:**
*   $P_{9\Omega} = 36 W$
*   $P_{11\Omega} = 44 W$
*   $P_{10\Omega} = 40 W$
*   $P_{5\Omega} = 180 W$
*   $P_{30\Omega} = 270 W$
*   $P_{4\Omega} = 100 W$
*   $P_{16\Omega} = 400 W$
*   $P_{15\Omega} = 240 W$

**c) $v_o = 190 V$.**

**d) A potência fornecida pela fonte de corrente ($1710 W$) é igual à potência absorvida por todos os outros elementos ($1710 W$).**


#Problema 2.28: 
a) Construa um modelo de circuito para esse dispositivo usando uma fonte ideal de tensão em série com um resistor.
b) Use o modelo para prever o valor de $i_t$ quando $v_t$ é igual a zero.

**Solução:**

**a) Construa um modelo de circuito para esse dispositivo usando uma fonte ideal de tensão em série com um resistor.**

Um modelo de circuito que consiste em uma fonte ideal de tensão em série com um resistor é conhecido como **equivalente de Thévenin**. A relação entre a tensão ($v_t$) e a corrente ($i_t$) para tal circuito é linear e pode ser expressa como:
$v_t = V_{Th} + R_{Th} i_t$
Onde $V_{Th}$ é a tensão de Thévenin (tensão de circuito aberto, quando $i_t = 0$) e $R_{Th}$ é a resistência de Thévenin.

**1. Encontrando $V_{Th}$ (Tensão de Circuito Aberto):**
A tensão de Thévenin é a tensão nos terminais do dispositivo quando a corrente $i_t$ é zero.
Pela tabela da Figura P2.28(b), quando $i_t = 0 A$, $v_t = 50 V$.
Portanto, $V_{Th} = 50 V$.

**2. Encontrando $R_{Th}$ (Resistência de Thévenin):**
A resistência de Thévenin pode ser encontrada a partir da inclinação da curva $v_t$ versus $i_t$. Como a relação é linear, podemos usar quaisquer dois pontos da tabela para calcular a inclinação:
$R_{Th} = \frac{\Delta v_t}{\Delta i_t}$

Usando os dois primeiros pontos da tabela (50 V, 0 A) e (66 V, 2 A):
$R_{Th} = \frac{66 V - 50 V}{2 A - 0 A} = \frac{16 V}{2 A} = 8 \Omega$.

**Modelo de Circuito:**
O dispositivo pode ser modelado como uma fonte de tensão ideal de **50 V** em série com um resistor de **8 Ω**. A polaridade da fonte de tensão deve ser tal que o terminal positivo esteja no mesmo lado do terminal positivo de $v_t$.

**b) Use o modelo para prever o valor de $i_t$ quando $v_t$ é igual a zero.**

Utilizamos o modelo de Thévenin que construímos:
$v_t = V_{Th} + R_{Th} i_t$
Substituímos $v_t = 0 V$, $V_{Th} = 50 V$ e $R_{Th} = 8 \Omega$:
$0 = 50 V + 8 \Omega \times i_t$
$8 \Omega \times i_t = -50 V$
$i_t = \frac{-50 V}{8 \Omega}$
$i_t = -6.25 A$

**Respostas:**
a) O modelo de circuito é uma fonte ideal de tensão de 50 V em série com um resistor de 8 Ω.
b) Quando $v_t = 0 V$, o valor de $i_t$ é $-6.25 A$.


# Problema 2.29:
a) Construa um modelo de circuito para esse dispositivo usando uma fonte ideal de corrente em paralelo com um resistor.
b) Use o modelo para prever a potência que o dispositivo fornecerá a um resistor de 20 Ω.

**Solução:**

**a) Construa um modelo de circuito para esse dispositivo usando uma fonte ideal de corrente em paralelo com um resistor.**

Um modelo de circuito que consiste em uma fonte ideal de corrente em paralelo com um resistor é conhecido como **equivalente de Norton**. Para converter os dados $v_t$ e $i_t$ para um equivalente de Norton, é útil primeiro encontrar o equivalente de Thévenin, pois a relação $v_t$ vs $i_t$ é linear.

A relação para o equivalente de Thévenin é $v_t = V_{Th} + R_{Th} i_t$.

**1. Encontrando $V_{Th}$ (Tensão de Circuito Aberto):**
A tensão de Thévenin é a tensão nos terminais do dispositivo quando a corrente $i_t$ é zero.
Pela tabela da Figura P2.29(b), quando $i_t = 0 A$, $v_t = 100 V$.
Portanto, $V_{Th} = 100 V$.

**2. Encontrando $R_{Th}$ (Resistência de Thévenin):**
A resistência de Thévenin pode ser encontrada a partir da inclinação da curva $v_t$ versus $i_t$. Usamos quaisquer dois pontos da tabela para calcular a inclinação:
$R_{Th} = \frac{\Delta v_t}{\Delta i_t}$

Usando os dois primeiros pontos da tabela (100 V, 0 A) e (120 V, 4 A):
$R_{Th} = \frac{120 V - 100 V}{4 A - 0 A} = \frac{20 V}{4 A} = 5 \Omega$.

**Convertendo para o Equivalente de Norton:**
Agora que temos o equivalente de Thévenin ($V_{Th} = 100 V$, $R_{Th} = 5 \Omega$), podemos convertê-lo para o equivalente de Norton.

A resistência de Norton ($R_N$) é igual à resistência de Thévenin:
$R_N = R_{Th} = 5 \Omega$.

A corrente de Norton ($I_N$) é a corrente de curto-circuito e pode ser calculada como:
$I_N = \frac{V_{Th}}{R_{Th}} = \frac{100 V}{5 \Omega} = 20 A$.

**Modelo de Circuito (Equivalente de Norton):**
O dispositivo pode ser modelado como uma fonte ideal de corrente de **20 A** em paralelo com um resistor de **5 Ω**. A direção da fonte de corrente deve ser tal que a corrente flua para fora do terminal positivo de $v_t$.

**b) Use o modelo para prever a potência que o dispositivo fornecerá a um resistor de 20 Ω.**

Conectamos um resistor de 20 Ω em paralelo com o equivalente de Norton (fonte de corrente de 20 A em paralelo com um resistor de 5 Ω).

Para encontrar a corrente que flui através do resistor de 20 Ω, podemos usar o divisor de corrente. A corrente total da fonte de Norton é 20 A. Ela se divide entre o resistor de 5 Ω e o resistor de 20 Ω.

A corrente através do resistor de 20 Ω ($I_{20\Omega}$) é:
$I_{20\Omega} = I_N \times \frac{R_N}{R_N + R_{carga}} = 20 A \times \frac{5 \Omega}{5 \Omega + 20 \Omega} = 20 A \times \frac{5}{25} = 20 A \times \frac{1}{5} = 4 A$.

A potência fornecida ao resistor de 20 Ω é $P = I^2 R$:
$P_{20\Omega} = (I_{20\Omega})^2 \times 20 \Omega = (4 A)^2 \times 20 \Omega = 16 \times 20 = 320 W$.

**Respostas:**
a) O modelo de circuito é uma fonte ideal de corrente de 20 A em paralelo com um resistor de 5 Ω.
b) A potência que o dispositivo fornecerá a um resistor de 20 Ω é 320 W.



#Problema 2.30:
a) Faça um gráfico de $i_s$ versus $v_s$.
b) Construa um modelo de circuito dessa fonte de corrente que seja válido para $0 \le v_s \le 75 V$, com base na equação da reta representada no gráfico em (a).
c) Use seu modelo de circuito para prever a corrente fornecida a um resistor de 2,5 kΩ.
d) Use seu modelo de circuito para prever a tensão de circuito aberto da fonte de corrente.
e) Qual é a tensão de circuito aberto real?
f) Explique por que as respostas para (d) e (e) não são iguais.

**Solução:**

**a) Faça um gráfico de $i_s$ versus $v_s$.**

Para fazer o gráfico, plotamos os pontos da tabela com $v_s$ no eixo x e $i_s$ no eixo y.

| $i_s$ (mA) | $v_s$ (V) | Ponto ($v_s, i_s$) |
| :--------- | :-------- | :----------------- |
| 20,0       | 0         | (0, 20.0)          |
| 17,5       | 25        | (25, 17.5)         |
| 15,0       | 50        | (50, 15.0)         |
| 12,5       | 75        | (75, 12.5)         |
| 9,0        | 100       | (100, 9.0)         |
| 4,0        | 125       | (125, 4.0)         |
| 0,0        | 140       | (140, 0.0)         |

Ao plotar esses pontos, observa-se que os primeiros quatro pontos (de $v_s = 0 V$ a $v_s = 75 V$) formam uma linha reta. Os pontos seguintes (para $v_s > 75 V$) se desviam dessa linha, indicando um comportamento não linear fora do intervalo inicial.
![graf](https://github.com/user-attachments/assets/b20feff1-dafe-4be4-9a49-0632be8c4446)

**b) Construa um modelo de circuito dessa fonte de corrente que seja válido para $0 \le v_s \le 75 V$, com base na equação da reta representada no gráfico em (a).**

Para o intervalo $0 \le v_s \le 75 V$, a relação entre $i_s$ e $v_s$ é linear. Um modelo para uma fonte real de corrente é uma fonte ideal de corrente em paralelo com um resistor (equivalente de Norton). A equação de uma linha reta é $i_s = m v_s + b$.

**1. Encontrando a inclinação (m):**
A inclinação representa o inverso da resistência em paralelo ($R_N$), ou seja, a condutância ($G_N$). Usando os pontos (0 V, 20.0 mA) e (75 V, 12.5 mA):
$m = \frac{\Delta i_s}{\Delta v_s} = \frac{12.5 mA - 20.0 mA}{75 V - 0 V} = \frac{-7.5 mA}{75 V} = -0.1 mA/V = -0.1 \times 10^{-3} A/V$.
A resistência em paralelo é $R_N = \frac{1}{|m|} = \frac{1}{0.1 \times 10^{-3}} = 10 \times 10^3 \Omega = 10 k\Omega$.

**2. Encontrando a interceptação no eixo y (b):**
A interceptação no eixo y é o valor de $i_s$ quando $v_s = 0 V$. Pela tabela, quando $v_s = 0 V$, $i_s = 20.0 mA$.
Portanto, $b = 20.0 mA$. Esta é a corrente da fonte ideal de corrente ($I_N$).

**Modelo de Circuito (Equivalente de Norton):**
O dispositivo pode ser modelado como uma fonte ideal de corrente de **20.0 mA** em paralelo com um resistor de **10 kΩ**. A direção da fonte de corrente deve ser tal que a corrente flua para fora do terminal positivo de $v_s$.

**c) Use seu modelo de circuito para prever a corrente fornecida a um resistor de 2,5 kΩ.**

Conectamos um resistor de 2,5 kΩ em paralelo com o modelo de Norton. Usamos o divisor de corrente:
$I_{2.5k\Omega} = I_N \times \frac{R_N}{R_N + R_{carga}}$
$I_{2.5k\Omega} = 20.0 mA \times \frac{10 k\Omega}{10 k\Omega + 2.5 k\Omega}$
$I_{2.5k\Omega} = 20.0 mA \times \frac{10}{12.5} = 20.0 mA \times 0.8$
$I_{2.5k\Omega} = 16.0 mA$.

**d) Use seu modelo de circuito para prever a tensão de circuito aberto da fonte de corrente.**

A tensão de circuito aberto ($V_{CA}$) é a tensão nos terminais do modelo quando a corrente de saída é zero ($i_s = 0$). No modelo de Norton, toda a corrente da fonte ($I_N$) passa pelo resistor em paralelo ($R_N$).
$V_{CA} = I_N \times R_N$
$V_{CA} = 20.0 mA \times 10 k\Omega = (20.0 \times 10^{-3} A) \times (10 \times 10^3 \Omega)$
$V_{CA} = 200 V$.

**e) Qual é a tensão de circuito aberto real?**

A tensão de circuito aberto real é o valor de $v_s$ quando $i_s = 0.0 mA$ na tabela fornecida.
Pela tabela, quando $i_s = 0.0 mA$, $v_s = 140 V$.
Portanto, a tensão de circuito aberto real é $140 V$.

**f) Explique por que as respostas para (d) e (e) não são iguais.**

As respostas para (d) e (e) não são iguais porque o modelo de circuito construído na parte (b) é válido apenas para o intervalo $0 \le v_s \le 75 V$. O modelo é baseado na suposição de uma relação linear entre $i_s$ e $v_s$ nesse intervalo. No entanto, a tabela mostra que a relação entre $i_s$ e $v_s$ não é linear para todo o intervalo de valores. A tensão de circuito aberto real (140 V) está fora do intervalo de validade do modelo linear, onde o comportamento do dispositivo não é mais linear.

**Respostas:**
a) O gráfico de $i_s$ versus $v_s$ mostra uma relação linear para $0 \le v_s \le 75 V$ e não linear para $v_s > 75 V$.
b) O modelo de circuito válido para $0 \le v_s \le 75 V$ é uma fonte ideal de corrente de 20.0 mA em paralelo com um resistor de 10 kΩ.
c) A corrente fornecida a um resistor de 2,5 kΩ é 16.0 mA.
d) A tensão de circuito aberto prevista pelo modelo é 200 V.
e) A tensão de circuito aberto real é 140 V.
f) As respostas para (d) e (e) não são iguais porque o modelo de circuito construído na parte (b) é válido apenas para o intervalo $0 \le v_s \le 75 V$. A tensão de circuito aberto real (140 V) está fora do intervalo de validade do modelo linear, onde o comportamento do dispositivo não é mais linear.


#Problema 2.31:
a) Faça um gráfico de $v_s$ versus $i_s$.
b) Construa um modelo de circuito da fonte real que seja válido para $0 \le i_s \le 24 mA$, com base na equação da reta representada no gráfico em (a). (Use uma fonte ideal de tensão em série com um resistor ideal.)
c) Use seu modelo de circuito para prever a corrente fornecida a um resistor de 1 kΩ conectado aos terminais de sua fonte real.
d) Use seu modelo de circuito para prever a corrente fornecida a um curto-circuito nos terminais da fonte real.
e) Qual é a corrente de curto-circuito real?
f) Explique por que as respostas para (d) e (e) não são iguais.

**Solução:**

**a) Faça um gráfico de $v_s$ versus $i_s$.**

Para fazer o gráfico, plotamos os pontos da tabela com $i_s$ no eixo x e $v_s$ no eixo y.

| $v_s$ (V) | $i_s$ (mA) | Ponto ($i_s, v_s$) |
| :-------- | :--------- | :----------------- |
| 24        | 0          | (0, 24)            |
| 22        | 8          | (8, 22)            |
| 20        | 16         | (16, 20)           |
| 18        | 24         | (24, 18)           |
| 15        | 32         | (32, 15)           |
| 10        | 40         | (40, 10)           |
| 0         | 48         | (48, 0)            |

Ao plotar esses pontos, observa-se que os primeiros quatro pontos (de $i_s = 0 mA$ a $i_s = 24 mA$) formam uma linha reta. Os pontos seguintes (para $i_s > 24 mA$) se desviam dessa linha, indicando um comportamento não linear fora do intervalo inicial.

![gra2](https://github.com/user-attachments/assets/c37d6055-e11f-4b2d-a46e-f0c4288ba6e5)

**b) Construa um modelo de circuito da fonte real que seja válido para $0 \le i_s \le 24 mA$, com base na equação da reta representada no gráfico em (a). (Use uma fonte ideal de tensão em série com um resistor ideal.)**

Para o intervalo $0 \le i_s \le 24 mA$, a relação entre $v_s$ e $i_s$ é linear. Um modelo para uma fonte real de tensão é uma fonte ideal de tensão em série com um resistor (equivalente de Thévenin). A equação de uma linha reta é $v_s = m i_s + b$.

**1. Encontrando a inclinação (m):**
A inclinação representa a resistência em série ($R_{Th}$). Usando os pontos (0 mA, 24 V) e (24 mA, 18 V):
$m = \frac{\Delta v_s}{\Delta i_s} = \frac{18 V - 24 V}{24 mA - 0 mA} = \frac{-6 V}{24 mA} = -0.25 V/mA = -0.25 \times 10^3 \Omega = -250 \Omega$.
A resistência de Thévenin é $R_{Th} = |m| = 250 \Omega$.

**2. Encontrando a interceptação no eixo y (b):**
A interceptação no eixo y é o valor de $v_s$ quando $i_s = 0 mA$.
Pela tabela, quando $i_s = 0 mA$, $v_s = 24 V$.
Portanto, $b = 24 V$. Esta é a tensão da fonte ideal de tensão ($V_{Th}$).

**Modelo de Circuito (Equivalente de Thévenin):**
O dispositivo pode ser modelado como uma fonte ideal de tensão de **24 V** em série com um resistor de **250 Ω**. A polaridade da fonte de tensão deve ser tal que o terminal positivo esteja no mesmo lado do terminal positivo de $v_s$.

**c) Use seu modelo de circuito para prever a corrente fornecida a um resistor de 1 kΩ conectado aos terminais de sua fonte real.**

Conectamos um resistor de 1 kΩ (1000 Ω) em série com o modelo de Thévenin.
A corrente total no circuito ($i_s$) será:
$i_s = \frac{V_{Th}}{R_{Th} + R_{carga}}$
$i_s = \frac{24 V}{250 \Omega + 1000 \Omega} = \frac{24 V}{1250 \Omega}$
$i_s = 0.0192 A = 19.2 mA$.

**d) Use seu modelo de circuito para prever a corrente fornecida a um curto-circuito nos terminais da fonte real.**

A corrente de curto-circuito ($I_{CC}$) é a corrente que flui quando $v_s = 0 V$. No modelo de Thévenin, isso ocorre quando os terminais de saída são curto-circuitados.
$I_{CC} = \frac{V_{Th}}{R_{Th}}$
$I_{CC} = \frac{24 V}{250 \Omega}$
$I_{CC} = 0.096 A = 96 mA$.

**e) Qual é a corrente de curto-circuito real?**

A corrente de curto-circuito real é o valor de $i_s$ quando $v_s = 0 V$ na tabela fornecida.
Pela tabela, quando $v_s = 0 V$, $i_s = 48 mA$.
Portanto, a corrente de curto-circuito real é $48 mA$.

**f) Explique por que as respostas para (d) e (e) não são iguais.**

As respostas para (d) e (e) não são iguais porque o modelo de circuito construído na parte (b) é válido apenas para o intervalo $0 \le i_s \le 24 mA$. A corrente de curto-circuito real (48 mA) está fora do intervalo de validade do modelo linear. O modelo linear não prevê com precisão o comportamento do dispositivo fora do intervalo para o qual foi projetado, onde o comportamento do dispositivo não é mais linear.

**Respostas:**
a) O gráfico de $v_s$ versus $i_s$ mostra uma relação linear para $0 \le i_s \le 24 mA$ e não linear para $i_s > 24 mA$.
b) O modelo de circuito válido para $0 \le i_s \le 24 mA$ é uma fonte ideal de tensão de 24 V em série com um resistor de 250 Ω.
c) A corrente fornecida a um resistor de 1 kΩ é 19.2 mA.
d) A corrente de curto-circuito prevista pelo modelo é 96 mA.
e) A corrente de curto-circuito real é 48 mA.
f) As respostas para (d) e (e) não são iguais porque o modelo de circuito construído na parte (b) é válido apenas para o intervalo $0 \le i_s \le 24 mA$. A corrente de curto-circuito real (48 mA) está fora do intervalo de validade do modelo linear, onde o comportamento do dispositivo não é mais linear.

Obrigado pela imagem do circuito e pelos cálculos para o Problema 2.33!

#Problema 2.33:

**Solução:**

Vamos seguir os passos fornecidos e depois calcular a potência total absorvida.

**1. Calcular a tensão $v_x$ usando o método de divisão de tensão:**

O circuito à esquerda da fonte dependente é um divisor de tensão simples. A tensão $v_x$ é a tensão sobre o resistor de 150 Ω.

$v_x = v_g \times \frac{150 \Omega}{150 \Omega + 450 \Omega}$
$v_x = 20 V \times \frac{150 \Omega}{600 \Omega}$
$v_x = 20 V \times \frac{1}{4}$
$v_x = 5 V$

Este cálculo está correto e coincide com o seu material.

**2. Determinar a corrente da fonte de corrente dependente, $i_x$:**

A fonte de corrente dependente é $\frac{v_x}{100}$.
$i_x = \frac{v_x}{100}$
$i_x = \frac{5 V}{100}$
$i_x = 0.05 A = 50 mA$

Este cálculo também está correto e coincide com o seu material.

**3. Aplicar a Lei de Ohm no resistor de 300 Ω para encontrar $v_o$:**

A fonte de corrente $i_x$ está em paralelo com o resistor de 300 Ω. A tensão $v_o$ é a tensão sobre o resistor de 300 Ω. A corrente $i_x$ flui para baixo através do resistor de 300 Ω, o que é consistente com a polaridade de $v_o$ (positivo em cima, negativo em baixo).

$v_o = i_x \times 300 \Omega$
$v_o = 0.05 A \times 300 \Omega$
$v_o = 15 V$

Este cálculo está correto e coincide com o seu material.

**4. Calcular a potência total absorvida no circuito:**

A potência total absorvida no circuito é a soma das potências absorvidas por todos os elementos passivos (resistores). Pelo princípio da conservação de energia, a potência total fornecida pelas fontes deve ser igual à potência total absorvida pelos elementos do circuito.

Vamos calcular a potência absorvida por cada resistor:

*   **Potência absorvida pelo resistor de 450 Ω ($P_{450\Omega}$):**
    A corrente que flui através do resistor de 450 Ω é a mesma que flui através do resistor de 150 Ω, que é a corrente fornecida pela fonte de 20 V.
    $I_{450\Omega} = \frac{20 V}{450 \Omega + 150 \Omega} = \frac{20 V}{600 \Omega} = \frac{1}{30} A$
    $P_{450\Omega} = I_{450\Omega}^2 \times 450 \Omega = \left(\frac{1}{30} A\right)^2 \times 450 \Omega = \frac{1}{900} \times 450 = 0.5 W$

*   **Potência absorvida pelo resistor de 150 Ω ($P_{150\Omega}$):**
    $P_{150\Omega} = I_{150\Omega}^2 \times 150 \Omega = \left(\frac{1}{30} A\right)^2 \times 150 \Omega = \frac{1}{900} \times 150 = \frac{1}{6} W \approx 0.1667 W$
    Alternativamente, $P_{150\Omega} = \frac{v_x^2}{150 \Omega} = \frac{(5V)^2}{150 \Omega} = \frac{25}{150} = \frac{1}{6} W \approx 0.1667 W$

*   **Potência absorvida pelo resistor de 300 Ω ($P_{300\Omega}$):**
    $P_{300\Omega} = \frac{v_o^2}{300 \Omega} = \frac{(15 V)^2}{300 \Omega} = \frac{225}{300} = 0.75 W$
    Alternativamente, $P_{300\Omega} = i_x^2 \times 300 \Omega = (0.05 A)^2 \times 300 \Omega = 0.0025 \times 300 = 0.75 W$

**Potência Total Absorvida pelos Resistores:**
$P_{total\_absorvida\_resistores} = P_{450\Omega} + P_{150\Omega} + P_{300\Omega}$
$P_{total\_absorvida\_resistores} = 0.5 W + \frac{1}{6} W + 0.75 W = \frac{1}{2} + \frac{1}{6} + \frac{3}{4} = \frac{6}{12} + \frac{2}{12} + \frac{9}{12} = \frac{17}{12} W \approx 1.4167 W$

**Verificação do Balanço de Potência (Potência Fornecida = Potência Absorvida):**

*   **Potência fornecida pela fonte de tensão de 20 V ($P_{20V}$):**
    A corrente que sai do terminal positivo da fonte de 20 V é $I_{450\Omega} = \frac{1}{30} A$. Como a corrente sai do terminal positivo, a fonte está **fornecendo** potência.
    $P_{20V} = V \times I = 20 V \times \frac{1}{30} A = \frac{2}{3} W \approx 0.6667 W$ (fornecida)

*   **Potência fornecida pela fonte de corrente dependente ($P_{dependente}$):**
    A tensão sobre a fonte de corrente dependente é $v_o = 15 V$. A corrente $i_x = 0.05 A$ flui na mesma direção da queda de tensão (de cima para baixo, positivo em cima). Portanto, a fonte de corrente dependente está **fornecendo** potência.
    $P_{dependente} = v_o \times i_x = 15 V \times 0.05 A = 0.75 W$ (fornecida)

**Potência Total Fornecida:**
$P_{total\_fornecida} = P_{20V} + P_{dependente} = \frac{2}{3} W + 0.75 W = 0.6667 W + 0.75 W = 1.4167 W$

Como $P_{total\_fornecida} \approx 1.4167 W$ e $P_{total\_absorvida\_resistores} \approx 1.4167 W$, o balanço de potência está correto.

**Respostas Finais:**
*   $v_o = 15 V$
*   A potência total absorvida no circuito (pelos resistores) é $\frac{17}{12} W \approx 1.4167 W$.


#Problema 2.34:
a) Determine $i_o$.
b) Verifique o valor de $i_o$, mostrando que a potência gerada no circuito é igual à potência absorvida no circuito.

**Solução:**

Vamos seguir os passos fornecidos e depois verificar o balanço de potência.

**a) Determine $i_o$.**

O circuito pode ser analisado como duas malhas independentes, pois a fonte de corrente de 10 mA está em um ramo que não compartilha diretamente um resistor com a segunda malha, e a tensão $v_1$ é a única ligação entre elas.

**Malha 1 (lado esquerdo):**
A fonte de corrente de 10 mA está em paralelo com o resistor de 4 kΩ. A tensão $v_1$ é a tensão sobre o resistor de 4 kΩ.
Usando a Lei de Ohm:
$v_1 = (10 mA) \times (4 k\Omega)$
$v_1 = (10 \times 10^{-3} A) \times (4 \times 10^3 \Omega)$
$v_1 = 40 V$

Este cálculo está correto e coincide com o seu material.

**Malha 2 (lado direito):**
A fonte de tensão dependente é $\frac{v_1}{2}$.
$v_x = \frac{v_1}{2}$
$v_x = \frac{40 V}{2}$
$v_x = 20 V$

Este cálculo também está correto e coincide com o seu material.

Agora, para encontrar $i_o$, que é a corrente que flui através dos resistores de 2 kΩ e 6 kΩ. Estes dois resistores estão em série na malha direita. A fonte de tensão dependente $v_x$ está em série com eles.
A corrente $i_o$ é a corrente total que flui através dessa série de resistores.
$i_o = \frac{v_x}{2 k\Omega + 6 k\Omega}$
$i_o = \frac{20 V}{8 k\Omega}$
$i_o = \frac{20 V}{8 \times 10^3 \Omega}$
$i_o = 2.5 \times 10^{-3} A = 2.5 mA$

Este cálculo está correto e coincide com o seu material.

**b) Verifique o valor de $i_o$, mostrando que a potência gerada no circuito é igual à potência absorvida no circuito.**

Vamos calcular a potência para cada elemento:

*   **Potência absorvida pelo resistor de 4 kΩ ($P_{4k\Omega}$):**
    $P_{4k\Omega} = \frac{v_1^2}{4 k\Omega} = \frac{(40 V)^2}{4000 \Omega} = \frac{1600}{4000} = 0.4 W$

*   **Potência absorvida pelo resistor de 2 kΩ ($P_{2k\Omega}$):**
    $P_{2k\Omega} = i_o^2 \times 2 k\Omega = (2.5 \times 10^{-3} A)^2 \times (2 \times 10^3 \Omega)$
    $P_{2k\Omega} = (6.25 \times 10^{-6}) \times (2 \times 10^3) = 0.0125 W$

*   **Potência absorvida pelo resistor de 6 kΩ ($P_{6k\Omega}$):**
    $P_{6k\Omega} = i_o^2 \times 6 k\Omega = (2.5 \times 10^{-3} A)^2 \times (6 \times 10^3 \Omega)$
    $P_{6k\Omega} = (6.25 \times 10^{-6}) \times (6 \times 10^3) = 0.0375 W$

*   **Potência gerada/absorvida pela fonte de corrente de 10 mA ($P_{10mA}$):**
    A tensão sobre a fonte de corrente é $v_1 = 40 V$. A corrente de 10 mA está saindo do terminal positivo da fonte. Portanto, a fonte está **gerando** potência.
    $P_{10mA} = V \times I = 40 V \times 10 mA = 40 V \times 10 \times 10^{-3} A = 0.4 W$ (gerada)

*   **Potência gerada/absorvida pela fonte de tensão dependente ($P_{dependente}$):**
    A tensão da fonte é $v_x = 20 V$. A corrente $i_o = 2.5 mA$ está saindo do terminal positivo da fonte de tensão dependente. Portanto, a fonte está **gerando** potência.
    $P_{dependente} = V \times I = 20 V \times 2.5 mA = 20 V \times 2.5 \times 10^{-3} A = 0.05 W$ (gerada)

**Potência Total Gerada:**
$P_{total\_gerada} = P_{10mA} + P_{dependente} = 0.4 W + 0.05 W = 0.45 W$

**Potência Total Absorvida:**
$P_{total\_absorvida} = P_{4k\Omega} + P_{2k\Omega} + P_{6k\Omega} = 0.4 W + 0.0125 W + 0.0375 W = 0.45 W$

Como $P_{total\_gerada} = P_{total\_absorvida} = 0.45 W$, o balanço de potência está verificado.

**Respostas:**
a) $i_o = 2.5 mA$
b) A potência gerada no circuito (0.45 W) é igual à potência absorvida no circuito (0.45 W).



#Problema 2.35:

**Solução:**

Vamos seguir os passos fornecidos e determinar as correntes solicitadas.

**a) Determine $i_o$.**

O problema afirma que o circuito é distribuído de forma que, se houver apenas um fio ligando duas malhas, a corrente que flui por esse fio é 0. No diagrama, $i_o$ é a corrente no fio que conecta a malha da esquerda com a malha da direita.

Primeiro, vamos calcular $v_\Delta$ e $i_x$ conforme o seu material.

**Cálculo de $v_\Delta$ (Malha 1 - lado esquerdo):**
A tensão $v_\Delta$ é a tensão sobre o resistor de 6 Ω. A fonte de 18 V está em série com os resistores de 12 Ω e 6 Ω. Podemos usar o divisor de tensão.
$v_\Delta = 18 V \times \frac{6 \Omega}{12 \Omega + 6 \Omega}$
$v_\Delta = 18 V \times \frac{6 \Omega}{18 \Omega}$
$v_\Delta = 18 V \times \frac{1}{3}$
$v_\Delta = 6 V$

Este cálculo está correto e coincide com o seu material.

**Cálculo de $i_x$ (Fonte de corrente dependente):**
A fonte de corrente dependente é $\frac{v_\Delta}{2}$.
$i_x = \frac{v_\Delta}{2}$
$i_x = \frac{6 V}{2}$
$i_x = 3 A$

Este cálculo também está correto e coincide com o seu material.

Agora, para determinar $i_o$, podemos usar a Análise Nodal. Vamos definir o nó inferior como referência (0 V).
Nó superior esquerdo (entre 12Ω e 6Ω): $V_A$
Nó superior direito (entre 6Ω, fonte dependente, 10Ω e 5Ω): $V_B$

A tensão $v_\Delta$ é a tensão no nó $V_A$ em relação ao nó de referência, então $V_A = v_\Delta = 6V$.

Aplicando a Lei das Correntes de Kirchhoff (LCK) no nó $V_A$:
A corrente que flui para baixo através do resistor de 6 Ω é $\frac{V_A}{6}$.
A corrente que flui para a direita através do ramo de $i_o$ é $i_o$.
A corrente que entra no nó $V_A$ vinda da fonte de 18V e do resistor de 12Ω é $\frac{18 - V_A}{12}$.

LCK no Nó $V_A$:
$\frac{18 - V_A}{12} = \frac{V_A}{6} + i_o$
Substituindo $V_A = 6V$:
$\frac{18 - 6}{12} = \frac{6}{6} + i_o$
$\frac{12}{12} = 1 + i_o$
$1 = 1 + i_o$
$i_o = 0 A$

Isso confirma a afirmação do seu material de que $i_o = 0 A$.

**b) Determine $i_1$.**

A corrente $i_1$ flui através do resistor de 10 Ω. A fonte de corrente dependente $i_x = 3 A$ está em paralelo com os resistores de 10 Ω e 5 Ω.
A corrente $i_1$ é a corrente que flui para baixo através do resistor de 10 Ω.
Podemos usar o divisor de corrente para encontrar $i_1$. A corrente total que entra no paralelo é $i_x = 3 A$.
$i_1 = i_x \times \frac{R_{outro}}{R_{total\_paralelo}}$
$i_1 = 3 A \times \frac{5 \Omega}{10 \Omega + 5 \Omega}$
$i_1 = 3 A \times \frac{5 \Omega}{15 \Omega}$
$i_1 = 3 A \times \frac{1}{3}$
$i_1 = 1 A$

**c) Determine $i_2$.**

A corrente $i_2$ flui através do resistor de 5 Ω.
Podemos usar o divisor de corrente para encontrar $i_2$.
$i_2 = i_x \times \frac{R_{outro}}{R_{total\_paralelo}}$
$i_2 = 3 A \times \frac{10 \Omega}{10 \Omega + 5 \Omega}$
$i_2 = 3 A \times \frac{10 \Omega}{15 \Omega}$
$i_2 = 3 A \times \frac{2}{3}$
$i_2 = 2 A$

**Verificação:**
$i_x = i_1 + i_2 = 1 A + 2 A = 3 A$. Isso está correto.

**Respostas:**
a) $i_o = 0 A$
b) $i_1 = 1 A$
c) $i_2 = 2 A$


# Problema P2.36
![lupi](https://github.com/user-attachments/assets/4e8ffd12-806e-4637-af68-1c44e1d1d1a0)


**Passo 1: Aplicando a lei de Kirchhoff para o primeiro Loop**

$-50 - 20i_b + 18i_\Delta = 0$

$18i_\Delta - 20i_\sigma - 50 = 0$ (1)

**Já para o segundo Loop**

$-18i_\Delta + 5i_\sigma + 40i_\sigma = 0$

$-18i_\Delta + 45i_\sigma = 0$ (2)

**Resolvendo as equações**

$i_\sigma = 2A$

$i_\Delta = 5A$

$v_0 = 40i_\sigma$

$v_0 = 40(2)$

$v_0 = 80V$

**Passo 2: Lei de Kirchhoff para Loop 3:**

$-20 + v_1 + v_0 = 0$

$-20 + v_1 + 80 = 0$

$v_1 = -60V$

**Agora a Lei do nó Kirchhoff no nó a:**

$i_1 - i_\sigma - 8i_\Delta = 0$

$i_1 - 2 - 8(5) = 0$

$i_1 = 42A$

**Novamente a Lei de Kirchhoff, agora aplicada ao nó b:**

$i_2 - i_\Delta - i_1 = 0$

$i_2 - 5 - 42 = 0$

$i_2 = 47A$

**Agora que finalmente encontramos as correntes, podemos finalmente encontrar as potências.**
Para fontes de tensão a potência é dada por $P = U I$, e para os resistores é $P = RI^2$
Então vamos:

$P_{50V} = -50(i_2) = -50(47) = -2350W$

$P_{20} = -20i_2 = -20(47) = -1880W$

$P_5 = 5i_\sigma i_1 = 5(2)(42) = 420W$

$P_8 = -v_1(8i_\Delta) = -(-60)(8)(5) = 2400W$

$P_{20} = 20(8i_\Delta) = 20(8)(5) = 800W$

$P_{18} = i_\Delta^2 18 = 5^2(18) = 450W$

$P_{40} = i_\sigma v_0 = 2(80) = 160W$

$P_{developed} = P_{50} + P_{20} = -2350 - 1880 = -4230 W$

$P_{absorbed} = P_5 + P_8 + P_{20} + P_{18} + P_{40}$

$= 420 + 2400 + 800 + 450 + 160$

$= 4230 W$

Obrigado pelas imagens do circuito e pelos cálculos para o Problema 2.37!

#Problema 2.37:

Vamos definir as correntes de malha no sentido horário:
*   Malha 1 (esquerda): $I_1$
*   Malha 2 (centro): $I_2$
*   Malha 3 (direita): $I_3$

**Relações com as variáveis do problema:**
*   $v_g = 147 V$ (conforme o diagrama, não 5V como na sua transcrição, que parece ser um erro de digitação ou um valor de exemplo). Vou usar 147V.
*   $v_1$ é a tensão no resistor de 1 Ω, então $v_1 = 1 \Omega \times I_1 = I_1$.
*   $v_o$ é a tensão no resistor de 10 Ω, então $v_o = 10 \Omega \times I_3$.
*   $i_1$ é a corrente no resistor de 20 Ω, então $i_1 = I_2$.
*   $i_2$ é a corrente no resistor de 10 Ω, então $i_2 = I_3$.

**Equações da Lei de Kirchhoff das Tensões (LKT):**

**Malha 1:**
$-147V + (1 \Omega)I_1 + (2 \Omega)(I_1 - I_2) = 0$
$3I_1 - 2I_2 = 147$ (Equação A)

**Malha 2:**
$-(2 \Omega)(I_2 - I_1) + (35 \Omega)(I_2 - I_3) + (20 \Omega)I_2 = 0$
$2I_1 - 2I_2 + 35I_2 - 35I_3 + 20I_2 = 0$
$2I_1 + 53I_2 - 35I_3 = 0$ (Equação B)

**Malha 3:**
$-(35 \Omega)(I_3 - I_2) + (10 \Omega)I_3 - (40 \Omega)i_2 = 0$
Substituindo $i_2 = I_3$:
$-35I_3 + 35I_2 + 10I_3 - 40I_3 = 0$
$35I_2 - 65I_3 = 0$ (Equação C)

**Resolvendo o sistema de equações (A, B, C):**

De (C), podemos expressar $I_2$ em termos de $I_3$:
$35I_2 = 65I_3 \implies I_2 = \frac{65}{35}I_3 = \frac{13}{7}I_3$

Substituindo $I_2$ na Equação A:
$3I_1 - 2\left(\frac{13}{7}I_3\right) = 147$
$3I_1 - \frac{26}{7}I_3 = 147$ (Equação D)

Substituindo $I_2$ na Equação B:
$2I_1 + 53\left(\frac{13}{7}I_3\right) - 35I_3 = 0$
$2I_1 + \frac{689}{7}I_3 - \frac{245}{7}I_3 = 0$
$2I_1 + \frac{444}{7}I_3 = 0$
$I_1 = -\frac{444}{14}I_3 = -\frac{222}{7}I_3$ (Equação E)

Agora, substituímos $I_1$ da Equação E na Equação D:
$3\left(-\frac{222}{7}I_3\right) - \frac{26}{7}I_3 = 147$
$-\frac{666}{7}I_3 - \frac{26}{7}I_3 = 147$
$-\frac{692}{7}I_3 = 147$
$I_3 = -\frac{147 \times 7}{692} = -\frac{1029}{692} \approx -1.48699 A$

Agora, calculamos $I_2$ e $I_1$:
$I_2 = \frac{13}{7}I_3 = \frac{13}{7} \times \left(-\frac{1029}{692}\right) = -\frac{13 \times 147}{692} = -\frac{1911}{692} \approx -2.76156 A$
$I_1 = -\frac{222}{7}I_3 = -\frac{222}{7} \times \left(-\frac{1029}{692}\right) = \frac{222 \times 147}{692} = \frac{32634}{692} \approx 47.15896 A$

**Determinando $v_1$ e $v_o$:**
$v_1 = I_1 \approx 47.159 V$
$v_o = 10 \Omega \times I_3 = 10 \Omega \times (-1.48699 A) \approx -14.870 V$

**Respostas:**
$v_1 \approx 47.16 V$
$v_o \approx -14.87 V$


Problema 2.38:

**Equações Iniciais :**

1.  $i_B + i_2 - i_1 = 0$
2.  $i_E - i_B - i_C = 0$
3.  $i_C = \beta i_B$
4.  $V_0 + i_E R_E - i_2 R_2 = 0$
5.  $-i_1 R_1 + V_{CC} - i_2 R_2 = 0$

**Passo 1: Utilizar (3) na (2) para expressar $i_E$ em função de $i_B$.**

Substitua $i_C = \beta i_B$ (Equação 3) na Equação 2 ($i_E - i_B - i_C = 0$):
$i_E - i_B - (\beta i_B) = 0$
$i_E = i_B + \beta i_B$
$i_E = i_B (1 + \beta)$

**Passo 2: Utilizar (1) para encontrar $i_2$ e então substituir em (4) e (5).**

Da Equação 1 ($i_B + i_2 - i_1 = 0$), isolamos $i_2$:
$i_2 = i_1 - i_B$

Agora, substituímos $i_2 = i_1 - i_B$ na Equação 4 ($V_0 + i_E R_E - i_2 R_2 = 0$):
$V_0 + i_E R_E - (i_1 - i_B) R_2 = 0$
$V_0 + i_E R_E - i_1 R_2 + i_B R_2 = 0$

Agora, substituímos $i_2 = i_1 - i_B$ na Equação 5 ($-i_1 R_1 + V_{CC} - i_2 R_2 = 0$):
$-i_1 R_1 + V_{CC} - (i_1 - i_B) R_2 = 0$
$-i_1 R_1 + V_{CC} - i_1 R_2 + i_B R_2 = 0$
$-i_1 (R_1 + R_2) + V_{CC} + i_B R_2 = 0$

Do resultado acima, isolamos $i_1$:
$i_1 (R_1 + R_2) = V_{CC} + i_B R_2$
$i_1 = \frac{V_{CC} + i_B R_2}{R_1 + R_2}$


**Próximos passos (para deduzir a Equação 2.25):**

1.  Substituir $i_E = i_B (1 + \beta)$ e $i_1 = \frac{V_{CC} + i_B R_2}{R_1 + R_2}$ na equação $V_0 + i_E R_E - i_1 R_2 + i_B R_2 = 0$.
2.  Rearranjar a equação resultante para isolar $i_B$.

Substituindo:
$V_0 + i_B (1 + \beta) R_E - \left(\frac{V_{CC} + i_B R_2}{R_1 + R_2}\right) R_2 + i_B R_2 = 0$

Distribuindo $R_2$ e separando os termos:
$V_0 + i_B (1 + \beta) R_E - \frac{V_{CC} R_2}{R_1 + R_2} - \frac{i_B R_2^2}{R_1 + R_2} + i_B R_2 = 0$

Agrupando os termos com $i_B$ no lado esquerdo e os termos sem $i_B$ no lado direito:
$i_B (1 + \beta) R_E - \frac{i_B R_2^2}{R_1 + R_2} + i_B R_2 = \frac{V_{CC} R_2}{R_1 + R_2} - V_0$

Fatorando $i_B$ do lado esquerdo:
$i_B \left[ (1 + \beta) R_E - \frac{R_2^2}{R_1 + R_2} + R_2 \right] = \frac{V_{CC} R_2}{R_1 + R_2} - V_0$

Simplificando o termo dentro dos colchetes:
$(1 + \beta) R_E + R_2 - \frac{R_2^2}{R_1 + R_2}$
$= (1 + \beta) R_E + \frac{R_2(R_1 + R_2) - R_2^2}{R_1 + R_2}$
$= (1 + \beta) R_E + \frac{R_1 R_2 + R_2^2 - R_2^2}{R_1 + R_2}$
$= (1 + \beta) R_E + \frac{R_1 R_2}{R_1 + R_2}$

Substituindo de volta na equação:
$i_B \left[ (1 + \beta) R_E + \frac{R_1 R_2}{R_1 + R_2} \right] = \frac{V_{CC} R_2}{R_1 + R_2} - V_0$

Finalmente, isolando $i_B$:
$i_B = \frac{\frac{V_{CC} R_2}{R_1 + R_2} - V_0}{(1 + \beta) R_E + \frac{R_1 R_2}{R_1 + R_2}}$

Obrigado pelas imagens do circuito e pelos cálculos para o Problema 2.39!

#Problema 2.39:

**Valores dos Componentes:**
*   $R_1 = 40 k\Omega = 40000 \Omega$
*   $R_2 = 60 k\Omega = 60000 \Omega$
*   $R_C = 750 \Omega$
*   $R_E = 120 \Omega$
*   $V_{CC} = 10 V$
*   $V_0 = 600 mV = 0.6 V$
*   $\beta = 49$

**Relações Importantes (do Exemplo 2.11 e Problema 2.38):**
*   $i_C = \beta i_B$
*   $i_E = i_B (1 + \beta)$
*   $i_2 = i_1 - i_B$
*   $i_1 = \frac{V_{CC} + i_B R_2}{R_1 + R_2}$
*   $i_B = \frac{\frac{V_{CC} R_2}{R_1 + R_2} - V_0}{(1 + \beta) R_E + \frac{R_1 R_2}{R_1 + R_2}}$ (Equação 2.25)

**Passo 1: Calcular $i_B$ usando a Equação 2.25.**

Primeiro, vamos calcular os termos da Equação 2.25:
*   $\frac{V_{CC} R_2}{R_1 + R_2} = \frac{10 V \times 60000 \Omega}{40000 \Omega + 60000 \Omega} = \frac{600000}{100000} = 6 V$
*   $\frac{R_1 R_2}{R_1 + R_2} = \frac{40000 \Omega \times 60000 \Omega}{40000 \Omega + 60000 \Omega} = \frac{2.4 \times 10^9}{100000} = 24000 \Omega = 24 k\Omega$
*   $(1 + \beta) R_E = (1 + 49) \times 120 \Omega = 50 \times 120 \Omega = 6000 \Omega = 6 k\Omega$

Agora, substitua na Equação 2.25:
$i_B = \frac{6 V - 0.6 V}{6000 \Omega + 24000 \Omega} = \frac{5.4 V}{30000 \Omega}$
$i_B = 0.00018 A = 0.18 mA$

**Passo 2: Calcular as outras correntes ($i_C, i_E, i_1, i_2, i_{CC}$).**

*   $i_C = \beta i_B = 49 \times 0.18 mA = 8.82 mA$
*   $i_E = (1 + \beta) i_B = 50 \times 0.18 mA = 9 mA$
*   $i_1 = \frac{V_{CC} + i_B R_2}{R_1 + R_2} = \frac{10 V + (0.18 \times 10^{-3} A \times 60000 \Omega)}{40000 \Omega + 60000 \Omega} = \frac{10 V + 10.8 V}{100000 \Omega} = \frac{20.8 V}{100000 \Omega}$
    $i_1 = 0.000208 A = 0.208 mA$
*   $i_2 = i_1 - i_B = 0.208 mA - 0.18 mA = 0.028 mA$
*   $i_{CC}$ (corrente na fonte $V_{CC}$)
    Da Equação (1) do Exemplo 2.11: $i_1 + i_C - i_{CC} = 0 \implies i_{CC} = i_1 + i_C$
    $i_{CC} = 0.208 mA + 8.82 mA = 9.028 mA$

**Passo 3: Calcular as tensões ($v_{3d}, v_{bd}, v_{ab}, v_{13}$).**

*   $v_{3d}$ (tensão no resistor $R_E$)
    $v_{3d} = i_E R_E = 9 mA \times 120 \Omega = 9 \times 10^{-3} A \times 120 \Omega = 1.08 V$
    (A Figura P2.39 mostra $v_{3d}$ como a tensão sobre $R_E$, com o terminal 3 positivo em relação a d.)

*   $v_{bd}$ (tensão entre o nó b e o nó d)
    $v_{bd} = i_2 R_2 = 0.028 mA \times 60000 \Omega = 0.028 \times 10^{-3} A \times 60000 \Omega = 1.68 V$

*   $v_{ab}$ (tensão entre o nó a e o nó b)
    $v_{ab} = i_1 R_1 = 0.208 mA \times 40000 \Omega = 0.208 \times 10^{-3} A \times 40000 \Omega = 8.32 V$

*   $v_{13}$ (tensão entre o nó 1 e o nó 3)
    $v_{13}$ é a tensão sobre o resistor $R_C$.
    $v_{13} = i_C R_C = 8.82 mA \times 750 \Omega = 8.82 \times 10^{-3} A \times 750 \Omega = 6.615 V$

**Respostas Finais:**
*   $i_B = 0.18 mA$
*   $i_C = 8.82 mA$
*   $i_E = 9 mA$
*   $i_1 = 0.208 mA$
*   $i_2 = 0.028 mA$
*   $i_{CC} = 9.028 mA$
*   $v_{3d} = 1.08 V$
*   $v_{bd} = 1.68 V$
*   $v_{ab} = 8.32 V$
*   $v_{13} = 6.615 V$
