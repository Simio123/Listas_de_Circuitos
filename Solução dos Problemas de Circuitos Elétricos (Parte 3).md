# Solução dos Problemas de Circuitos Elétricos (Parte 3)

A seguir, apresentamos as soluções detalhadas para os problemas de circuito solicitados (2.18, 2.23, 2.24, 2.25, 2.26, 2.30, 2.31 e 2.33 a 2.39), extraídos do arquivo PDF fornecido.

## Problema 2.18

**Objetivo:** Determinar correntes, tensão e potências em um circuito com fonte dependente.

**Circuito:** Conforme a Figura P2.18, temos uma fonte de tensão independente de 50V, resistores de 1kΩ, 4kΩ, 2kΩ e 3kΩ, e uma fonte de corrente dependente. A fonte dependente é indicada como "4ia" com a seta apontando para cima, conectada entre os nós que unem os resistores 1kΩ/4kΩ e 2kΩ/3kΩ. Assumimos que se trata de uma fonte de corrente controlada por corrente (CCCS) com ganho 4, cujo valor é `4 * ia`. A corrente de controle `ia` é a corrente que desce pelo resistor de 2kΩ. A corrente `ib` desce pelo resistor de 3kΩ, e a tensão `vo` está sobre o resistor de 3kΩ com polaridade positiva no topo.

**Análise (Método Nodal):**
Definimos o nó inferior como referência (0V). Existem dois nós essenciais além da referência:
*   Nó 1: Junção dos resistores de 1kΩ, 4kΩ e da fonte dependente. Tensão `V1`.
*   Nó 2: Junção dos resistores de 2kΩ, 3kΩ e da fonte dependente. Tensão `V2`.
O nó acima da fonte de 50V está a 50V em relação à referência.

As variáveis de interesse em termos das tensões nodais são:
*   `ia = (V2 - 0V) / 2kΩ = V2 / 2k`
*   `ib = (V2 - 0V) / 3kΩ = V2 / 3k`
*   `vo = V2 - 0V = V2`

Aplicamos a Lei das Correntes de Kirchhoff (KCL) aos nós 1 e 2 (soma das correntes que saem = 0):
*   **Nó 1:** `(V1 - 50V) / 1kΩ + V1 / 4kΩ + 4 * ia = 0`
*   **Nó 2:** `V2 / 2kΩ + V2 / 3kΩ - 4 * ia = 0`

Substituímos `ia = V2 / 2k` nas equações KCL:
*   Nó 1: `(V1 - 50)/1k + V1/4k + 4*(V2/2k) = 0`
*   Nó 2: `V2/2k + V2/3k - 4*(V2/2k) = 0`

Simplificamos as equações:
*   Nó 1 (multiplicando por 4k): `4(V1 - 50) + V1 + 8V2 = 0` => `5V1 + 8V2 = 200`
*   Nó 2 (multiplicando por 6k): `3V2 + 2V2 - 12V2 = 0` => `-7V2 = 0` => `V2 = 0 V`

Substituindo `V2 = 0` na equação do Nó 1:
`5V1 + 8(0) = 200` => `5V1 = 200` => `V1 = 40 V`

**Cálculos dos Resultados:**
*   **(a) Valor de `ia`:**
    `ia = V2 / 2k = 0 V / 2000 Ω = 0 A`
*   **(b) Valor de `ib`:**
    `ib = V2 / 3k = 0 V / 3000 Ω = 0 A`
*   **(c) Valor de `vo`:**
    `vo = V2 = 0 V`
*   **(d) Potência dissipada em cada resistor:**
    *   P(1kΩ): `P = (V_fonte - V1)^2 / R = (50V - 40V)^2 / 1000Ω = (10V)^2 / 1000Ω = 100 / 1000 = 0.1 W = 100 mW`
    *   P(4kΩ): `P = V1^2 / R = (40V)^2 / 4000Ω = 1600 / 4000 = 0.4 W = 400 mW`
    *   P(2kΩ): `P = V2^2 / R = (0V)^2 / 2000Ω = 0 W`
    *   P(3kΩ): `P = V2^2 / R = (0V)^2 / 3000Ω = 0 W`
*   **(e) Potência fornecida pela fonte de 50 V:**
    A corrente que sai do terminal positivo da fonte é `I_fonte = (50V - V1) / 1kΩ = (50V - 40V) / 1000Ω = 10V / 1000Ω = 0.01 A`.
    `P_fornecida(50V) = V_fonte * I_fonte = 50V * 0.01A = 0.5 W = 500 mW`

**Verificação do Balanço de Potência:**
A potência fornecida pela fonte dependente é `P_dep = V_dep * I_dep`. A tensão sobre a fonte dependente é `V1 - V2 = 40V - 0V = 40V`. A corrente fornecida é `4*ia = 4*0 = 0A`. Logo, `P_dep = 40V * 0A = 0W`.
A potência total fornecida é `P_total_fornecida = P_fornecida(50V) + P_dep = 500 mW + 0 mW = 500 mW`.
A potência total dissipada nos resistores é `P_total_dissipada = P(1kΩ) + P(4kΩ) + P(2kΩ) + P(3kΩ) = 100 mW + 400 mW + 0 W + 0 W = 500 mW`.
Como `P_total_fornecida = P_total_dissipada`, o balanço de potência está correto.

**Respostas 2.18:**
(a) `ia = 0 A`
(b) `ib = 0 A`
(c) `vo = 0 V`
(d) P(1kΩ) = 100 mW, P(4kΩ) = 400 mW, P(2kΩ) = 0 W, P(3kΩ) = 0 W
(e) P_fornecida(50V) = 500 mW

---



## Problema 2.23

**Objetivo:** Determinar o valor de um resistor variável para atingir uma corrente específica.

**Circuito:** Conforme a Figura P2.23, uma fonte de 80V está em série com um resistor de 1.5kΩ. Este conjunto alimenta uma combinação paralela. Um ramo paralelo contém um resistor de 3kΩ (com corrente `io` descendo). O outro ramo paralelo contém o resistor variável R em série com um resistor de 5kΩ.

**Condição:** O resistor R é ajustado para que `io = 10 mA`.

**Análise:**
1.  **Tensão na Combinação Paralela (`Vp`):** A tensão sobre o resistor de 3kΩ é a mesma que a tensão sobre o ramo com R e 5kΩ. Usando a Lei de Ohm no ramo de 3kΩ:
    `Vp = io * 3kΩ = (10 mA) * (3000 Ω) = (0.010 A) * (3000 Ω) = 30 V`.

2.  **Corrente Total (`Itotal`):** Aplicamos a Lei das Tensões de Kirchhoff (KVL) na malha principal (fonte, resistor de 1.5kΩ e a combinação paralela):
    `80 V = Itotal * 1.5kΩ + Vp`
    `80 V = Itotal * 1500 Ω + 30 V`
    `Itotal * 1500 Ω = 80 V - 30 V = 50 V`
    `Itotal = 50 V / 1500 Ω = 1/30 A ≈ 33.33 mA`.

3.  **Corrente no Ramo de R (`I_R_branch`):** Aplicamos a Lei das Correntes de Kirchhoff (KCL) no nó superior da combinação paralela. A corrente total `Itotal` se divide entre `io` e a corrente no ramo de R (`I_R_branch`):
    `Itotal = io + I_R_branch`
    `1/30 A = 10 mA + I_R_branch`
    `1/30 A = 0.010 A + I_R_branch`
    `I_R_branch = (1/30 - 0.010) A = (1/30 - 1/100) A = (10/300 - 3/300) A = 7/300 A ≈ 23.33 mA`.

4.  **Valor de R:** Aplicamos a Lei de Ohm ao ramo que contém R e 5kΩ. A tensão total neste ramo é `Vp`, e a corrente é `I_R_branch`. A resistência total do ramo é `R + 5kΩ`.
    `Vp = I_R_branch * (R + 5kΩ)`
    `30 V = (7/300 A) * (R + 5000 Ω)`
    `R + 5000 Ω = 30 V / (7/300 A) = (30 * 300) / 7 Ω = 9000 / 7 Ω ≈ 1285.71 Ω`
    `R = (9000 / 7) Ω - 5000 Ω = (9000 - 35000) / 7 Ω = -26000 / 7 Ω ≈ -3714.29 Ω`.

**Conclusão:** O cálculo resulta em um valor negativo para a resistência R (`R ≈ -3.71 kΩ`). Uma resistência passiva não pode ter valor negativo. Isso indica que, com a configuração dada, não é possível obter `io = 10 mA` ajustando um resistor R passivo. Pode haver um erro no enunciado do problema, no diagrama ou nos valores fornecidos.

**Resposta 2.23:** Com base nos cálculos, não existe valor de R (resistência passiva) que satisfaça `io = 10 mA`. O valor calculado é `R ≈ -3.71 kΩ`.

---



## Problema 2.24

**Objetivo:** Determinar um resistor desconhecido e a potência fornecida pela fonte em um circuito resistivo.

**Circuito:** Conforme a Figura P2.24, uma fonte de 240V está conectada em série com um resistor de 5Ω. Após este resistor, o circuito se divide em dois ramos paralelos. O ramo superior contém apenas o resistor desconhecido R. O ramo inferior contém um resistor de 4Ω em série com uma combinação paralela mais complexa. Uma corrente de 4A é indicada fluindo para baixo através do resistor de 4Ω. A combinação paralela interna consiste em um resistor de 10Ω em paralelo com um ramo contendo um resistor de 6Ω em série com outra combinação paralela (um resistor de 10Ω em paralelo com um resistor de 14Ω).

**Análise e Cálculos:**
Vamos simplificar o circuito passo a passo, começando pela combinação paralela mais interna.
1.  **Resistência Equivalente (10Ω || 14Ω):**
    `Req1 = (10 * 14) / (10 + 14) = 140 / 24 = 35 / 6 Ω`.
2.  **Resistência do Ramo Interno (6Ω + Req1):**
    `R_ramo_interno = 6Ω + Req1 = 6 + 35/6 = (36 + 35) / 6 = 71 / 6 Ω`.
3.  **Resistência Equivalente (10Ω || R_ramo_interno):**
    `Req2 = (10 * R_ramo_interno) / (10 + R_ramo_interno) = (10 * 71/6) / (10 + 71/6) = (710/6) / ((60 + 71)/6) = (710/6) / (131/6) = 710 / 131 Ω`.
    Esta é a resistência equivalente da combinação paralela complexa que está em série com o resistor de 4Ω.
4.  **Tensão no Ramo Inferior (`V_ramo_inf`):** O ramo inferior principal (excluindo R) consiste no resistor de 4Ω em série com `Req2`. A corrente que flui por este ramo é dada como 4A.
    *   Tensão sobre o resistor de 4Ω: `V_4ohm = 4A * 4Ω = 16 V`.
    *   Tensão sobre `Req2`: `V_Req2 = 4A * Req2 = 4 * (710 / 131) = 2840 / 131 V`.
    *   Tensão total no ramo inferior (que também é a tensão sobre o resistor R): `V_paralelo = V_4ohm + V_Req2 = 16 + 2840/131 = (16*131 + 2840)/131 = (2096 + 2840)/131 = 4936 / 131 V`.
5.  **Tensão sobre o Resistor de 5Ω (`V_5ohm`):** Aplicando KVL na malha externa:
    `240 V = V_5ohm + V_paralelo`
    `V_5ohm = 240 - V_paralelo = 240 - 4936/131 = (240*131 - 4936)/131 = (31440 - 4936)/131 = 26504 / 131 V`.
6.  **Corrente Total (`Itotal`):** A corrente total fornecida pela fonte passa pelo resistor de 5Ω.
    `Itotal = V_5ohm / 5Ω = (26504 / 131 V) / 5 Ω = 26504 / (131 * 5) = 26504 / 655 A`.
7.  **Corrente no Resistor R (`I_R`):** Aplicando KCL no nó após o resistor de 5Ω:
    `Itotal = I_R + I_ramo_inf` (onde `I_ramo_inf = 4A`)
    `I_R = Itotal - 4A = (26504 / 655) - 4 = (26504 - 4*655) / 655 = (26504 - 2620) / 655 = 23884 / 655 A`.
8.  **(a) Valor de R:** Usando a Lei de Ohm para o resistor R:
    `R = V_paralelo / I_R = (4936 / 131 V) / (23884 / 655 A)`
    `R = (4936 / 131) * (655 / 23884) = (4936 / 131) * (131 * 5 / 23884)`
    `R = (4936 * 5) / 23884 = 24680 / 23884 Ω ≈ 1.033 Ω`.
9.  **(b) Potência fornecida pela fonte de 240 V:**
    `P_fornecida = V_fonte * Itotal = 240 V * (26504 / 655 A)`
    `P_fornecida = (240 * 26504) / 655 = 6360960 / 655 W ≈ 9711.4 W ≈ 9.71 kW`.

**Respostas 2.24:**
(a) `R ≈ 1.033 Ω`
(b) Potência fornecida ≈ `9711.4 W` (ou 9.71 kW)

---



## Problema 2.25

**Objetivo:** Calcular potências dissipadas e fornecida em um circuito resistivo complexo.

**Circuito:** Conforme a Figura P2.25, uma fonte de 125V está conectada a uma rede série-paralelo de resistores (1Ω, 15Ω, 5Ω, 30Ω, 16Ω, 4Ω).

**Dado Adicional (e Inconsistente):** O enunciado afirma que a tensão no resistor de 16Ω é 80V (positiva no terminal superior). Como veremos, este dado é inconsistente com o valor da fonte de 125V e a configuração do circuito. Para responder às perguntas sobre potências dissipadas e fornecida pela fonte de 125V, assumiremos que o valor da fonte (125V) está correto e ignoraremos a informação dos 80V sobre o resistor de 16Ω.

**Análise (Assumindo Fonte de 125V):**
Primeiro, calculamos a resistência equivalente total vista pela fonte.
1.  Resistência série interna: `R_si = 16Ω + 4Ω = 20Ω`.
2.  Resistência paralela interna: `R_pi = (30Ω * R_si) / (30Ω + R_si) = (30 * 20) / (30 + 20) = 600 / 50 = 12Ω`.
3.  Resistência do ramo série externo: `R_se = 5Ω + R_pi = 5Ω + 12Ω = 17Ω`.
4.  Resistência paralela externa: `R_pe = (15Ω * R_se) / (15Ω + R_se) = (15 * 17) / (15 + 17) = 255 / 32 Ω`.
5.  Resistência total equivalente: `R_total = 1Ω + R_pe = 1 + 255/32 = (32 + 255) / 32 = 287 / 32 Ω`.

Agora, calculamos as correntes e tensões necessárias:
*   Corrente total fornecida pela fonte: `Itotal = V_fonte / R_total = 125V / (287/32 Ω) = (125 * 32) / 287 = 4000 / 287 A`.
*   Tensão na combinação paralela externa (`V_pe`): `V_pe = Itotal * R_pe = (4000/287 A) * (255/32 Ω) = (125 * 255) / 287 = 31875 / 287 V`.
*   Corrente no resistor de 15Ω (`I_15`): `I_15 = V_pe / 15Ω = (31875/287 V) / 15Ω = 2125 / 287 A`.
*   Corrente no ramo série externo (`I_se`, que passa pelo resistor de 5Ω): `I_se = V_pe / R_se = (31875/287 V) / 17Ω = 1875 / 287 A`.
*   Tensão na combinação paralela interna (`V_pi`): `V_pi = I_se * R_pi = (1875/287 A) * 12Ω = 22500 / 287 V`.
*   Corrente no resistor de 30Ω (`I_30`): `I_30 = V_pi / 30Ω = (22500/287 V) / 30Ω = 750 / 287 A`.
*   Corrente no ramo série interno (`I_si`, que passa pelos resistores de 16Ω e 4Ω): `I_si = V_pi / R_si = (22500/287 V) / 20Ω = 1125 / 287 A`.

*(Verificação da inconsistência: A tensão no resistor de 16Ω seria `V_16 = I_si * 16Ω = (1125/287 A) * 16Ω = 18000 / 287 V ≈ 62.7 V`, que é diferente dos 80V mencionados no enunciado.)*

**Cálculos das Potências:**
*   **(a) Potência dissipada em cada resistor:**
    *   P(1Ω) = `Itotal^2 * 1Ω = (4000/287)^2 * 1 = 16000000 / 82369 W ≈ 194.24 W`
    *   P(15Ω) = `I_15^2 * 15Ω = (2125/287)^2 * 15 = 67734375 / 82369 W ≈ 822.32 W`
    *   P(5Ω) = `I_se^2 * 5Ω = (1875/287)^2 * 5 = 17578125 / 82369 W ≈ 213.40 W`
    *   P(30Ω) = `I_30^2 * 30Ω = (750/287)^2 * 30 = 16875000 / 82369 W ≈ 204.87 W`
    *   P(16Ω) = `I_si^2 * 16Ω = (1125/287)^2 * 16 = 20250000 / 82369 W ≈ 245.85 W`
    *   P(4Ω) = `I_si^2 * 4Ω = (1125/287)^2 * 4 = 5062500 / 82369 W ≈ 61.46 W`
*   **(b) Potência fornecida pela fonte de 125 V:**
    *   `P_fornecida = V_fonte * Itotal = 125V * (4000 / 287 A) = 500000 / 287 W ≈ 1742.16 W`
*   **(c) Verificação do balanço de potência:**
    *   `P_total_dissipada = P(1Ω) + P(15Ω) + P(5Ω) + P(30Ω) + P(16Ω) + P(4Ω)`
    *   `P_total_dissipada = (16000000 + 67734375 + 17578125 + 16875000 + 20250000 + 5062500) / 82369`
    *   `P_total_dissipada = 143500000 / 82369 W`
    *   Comparando com a potência fornecida: `P_fornecida = 500000 / 287 = (500000 * 287) / (287 * 287) = 143500000 / 82369 W`.
    *   A potência total dissipada é igual à potência fornecida, confirmando os cálculos.

**Respostas 2.25 (baseadas na fonte de 125V):**
(a) Potências dissipadas:
    P(1Ω) ≈ 194.24 W
    P(15Ω) ≈ 822.32 W
    P(5Ω) ≈ 213.40 W
    P(30Ω) ≈ 204.87 W
    P(16Ω) ≈ 245.85 W
    P(4Ω) ≈ 61.46 W
(b) Potência fornecida pela fonte de 125V ≈ 1742.16 W
(c) Verificado: Potência total fornecida ≈ Potência total dissipada ≈ 1742.16 W.

---



## Problema 2.26

**Objetivo:** Determinar fontes desconhecidas e verificar o balanço de potência.

**Circuito:** Conforme a Figura P2.26, temos uma fonte de corrente `ig` e uma fonte de tensão `vg` em uma rede resistiva (11Ω, 9Ω, 30Ω, 5Ω, 10Ω, 15Ω).

**Dados:** Corrente `ia = 4 A` (descendo pelo resistor de 15Ω) e `ib = -2 A` (descendo pelo resistor de 10Ω).

**Análise (Método Nodal):**
Definimos o nó inferior como referência (0V). Sejam `V1`, `V2`, `V3` as tensões nos nós essenciais (ver descrição no problema 2.26 do PDF).
1.  **Tensão V2:** A corrente `ib` desce pelo resistor de 10Ω (conectado entre o nó 2 e a referência). `V2 = ib * 10Ω = (-2 A) * 10Ω = -20 V`.
2.  **Relação V3 e vg:** A corrente `ia` desce pelo resistor de 15Ω (conectado entre o terminal positivo de `vg` e o nó 3). Assumindo que o terminal negativo de `vg` está na referência, a tensão no terminal positivo é `vg`. Portanto, `(vg - V3) / 15Ω = ia = 4 A`, o que implica `vg - V3 = 60 V` ou `vg = V3 + 60`.
3.  **KCL no Nó 2 (V2 = -20V):** Correntes saindo: `ib` (para baixo), `(V2-V1)/9Ω` (para esquerda), `(V2-V3)/5Ω` (para direita).
    `ib + (V2 - V1)/9 + (V2 - V3)/5 = 0`
    `-2 + (-20 - V1)/9 + (-20 - V3)/5 = 0`
    Multiplicando por 45: `-90 + 5(-20 - V1) + 9(-20 - V3) = 0`
    `-90 - 100 - 5V1 - 180 - 9V3 = 0`
    `5V1 + 9V3 = -370` (Equação 1)
4.  **KCL no Nó 3:** Correntes entrando: `ia` (de cima), `(V2-V3)/5Ω` (da esquerda). Corrente saindo: `(V3-V1)/30Ω` (para esquerda).
    `ia + (V2 - V3)/5 = (V3 - V1)/30`
    `4 + (-20 - V3)/5 = (V3 - V1)/30`
    Multiplicando por 30: `120 + 6(-20 - V3) = V3 - V1`
    `120 - 120 - 6V3 = V3 - V1`
    `V1 = 7V3` (Equação 2)
5.  **Resolvendo V1 e V3:** Substituindo (2) em (1):
    `5(7V3) + 9V3 = -370`
    `35V3 + 9V3 = -370`
    `44V3 = -370` => `V3 = -370 / 44 = -185 / 22 V ≈ -8.41 V`
    `V1 = 7 * V3 = 7 * (-185 / 22) = -1295 / 22 V ≈ -58.86 V`

**Cálculos dos Resultados:**
*   **(a) Determinar `ig`:** Assumindo que `ig` flui da referência para o nó 1 e que o resistor de 11Ω conecta o nó 1 à referência. KCL no Nó 1:
    `ig = (V1 - V2)/9 + (V1 - V3)/30 + V1/11`
    `ig = (-1295/22 - (-20))/9 + (-1295/22 - (-185/22))/30 + (-1295/22)/11`
    `ig = (-855/22)/9 + (-1110/22)/30 - 1295/242`
    `ig = -95/22 - 111/66 - 1295/242 = -95/22 - 37/22 - 1295/242`
    `ig = -132/22 - 1295/242 = -6 - 1295/242 = (-1452 - 1295)/242 = -2747 / 242 A ≈ -11.35 A`
*   **(b) Determinar `vg`:**
    `vg = V3 + 60 = -185/22 + 60 = (-185 + 1320)/22 = 1135 / 22 V ≈ 51.59 V`
*   **(c) Determinar `vg`:** (Repetido no enunciado, assumindo confirmação do valor)
    `vg = 1135 / 22 V ≈ 51.59 V`
*   **(d) Mostrar que a potência fornecida pela fonte de corrente é igual à potência absorvida por todos os outros elementos:** Esta afirmação parece incorreta, pois temos duas fontes (`ig` e `vg`). A verificação correta é se a potência total fornecida pelas fontes é igual à potência total absorvida pelos resistores.
    *   **Potência Absorvida pelos Resistores:**
        P(11Ω) ≈ 315.0 W
        P(9Ω) ≈ 167.8 W
        P(30Ω) ≈ 84.9 W
        P(5Ω) ≈ 26.9 W
        P(10Ω) = 40.0 W
        P(15Ω) = 240.0 W
        **Total P_abs (Resistores) ≈ 874.6 W**
    *   **Potência Fornecida pelas Fontes:**
        P_supp(vg) = `vg * ia = (1135/22 V) * 4 A = 2270 / 11 W ≈ 206.4 W` (Fornecida)
        P_supp(ig) = `-V1 * ig = -(-1295/22 V) * (-2747/242 A) = -3557165 / 5324 W ≈ -668.2 W` (Absorvida)
        **Total P_supp (Fontes) = P_supp(vg) + P_supp(ig) ≈ 206.4 W - 668.2 W = -461.8 W**
    *   **Verificação:** A potência total absorvida pelos resistores (≈ 874.6 W) não é igual à potência total fornecida pelas fontes (≈ -461.8 W). O balanço de potência não fecha. Isso sugere fortemente um erro nos valores dados (`ia`, `ib`), na configuração do circuito no diagrama, ou na própria questão (d).

**Respostas 2.26 (com ressalva sobre o balanço de potência):**
(a) `ig = -2747 / 242 A ≈ -11.35 A`
(b) `vg = 1135 / 22 V ≈ 51.59 V`
(c) `vg = 1135 / 22 V ≈ 51.59 V`
(d) O balanço de potência não foi verificado com os dados fornecidos. P_total_absorvida ≈ 874.6 W ≠ P_total_fornecida ≈ -461.8 W.

---



## Problema 2.30

**Objetivo:** Analisar dados de uma fonte de corrente real e construir um modelo de circuito.

**Dados:** A tabela na Figura P2.30(a) relaciona a corrente terminal `is` e a tensão terminal `vs` para a fonte de corrente constante (FCC) real mostrada na Figura P2.30(b).

| `is` (mA) | `vs` (V) |
| :-------- | :------- |
| 20.0      | 0        |
| 17.5      | 25       |
| 15.0      | 50       |
| 12.5      | 75       |
| 9.0       | 100      |
| 4.0       | 125      |
| 0.0       | 140      |

**Análise e Cálculos:**

*   **(a) Faça um gráfico de `is` versus `vs`.**
    O gráfico de `is` (eixo y, em mA) versus `vs` (eixo x, em V) mostraria os pontos da tabela. Observando os primeiros quatro pontos (para `0 <= vs <= 75 V`), a relação é linear. A inclinação `m = Δis / Δvs = (17.5 - 20.0) / (25 - 0) = -2.5 / 25 = -0.1 mA/V`. A interceptação no eixo `is` (quando `vs = 0`) é `b = 20.0 mA`. A equação da reta para esta faixa é `is = -0.1 * vs + 20` (com `is` em mA, `vs` em V). Para `vs > 75 V`, a inclinação muda, indicando um comportamento não linear da fonte real fora dessa faixa.

*   **(b) Construa um modelo de circuito dessa fonte de corrente que seja válido para `0 <= vs <= 75 V`, com base na equação da reta representada no gráfico em (a).**
    O modelo de circuito para uma fonte de corrente real é o equivalente de Norton: uma fonte de corrente ideal `I_N` em paralelo com uma resistência interna `R_N`. A relação terminal é `is = I_N - vs / R_N`.
    Comparando com a equação linear derivada em (a), `is = -0.1 * vs + 20` (convertendo para Amperes: `is = -0.0001 * vs + 0.020`):
    *   A corrente da fonte ideal `I_N` é o valor de `is` quando `vs = 0`, que é `I_N = 20 mA` (ou 0.020 A).
    *   O termo `-vs / R_N` corresponde a `-0.0001 * vs`. Portanto, `1 / R_N = 0.0001 A/V` (ou 0.1 mA/V).
    *   `R_N = 1 / 0.0001 = 10000 Ω = 10 kΩ`.
    O modelo válido para `0 <= vs <= 75 V` é uma fonte de corrente ideal de 20 mA em paralelo com um resistor de 10 kΩ.

*   **(c) Use seu modelo de circuito para prever a corrente fornecida a um resistor de 2,5 kΩ.**
    Conectamos uma carga `R_L = 2.5 kΩ` aos terminais do modelo de Norton. A corrente `I_N = 20 mA` se divide entre `R_N = 10 kΩ` e `R_L = 2.5 kΩ`. Usando o divisor de corrente para encontrar a corrente na carga (`is`):
    `is = I_N * (R_N / (R_N + R_L))`
    `is = 20 mA * (10 kΩ / (10 kΩ + 2.5 kΩ))`
    `is = 20 mA * (10 / 12.5) = 20 mA * 0.8 = 16 mA`.
    O modelo prevê que a fonte fornecerá 16 mA ao resistor de 2.5 kΩ.

*   **(d) Use seu modelo de circuito para prever a tensão de circuito aberto da fonte de corrente.**
    A tensão de circuito aberto (`vs_oc`) ocorre quando `is = 0`. Usando a equação do modelo `is = I_N - vs / R_N`:
    `0 = 20 mA - vs_oc / 10 kΩ`
    `vs_oc / 10 kΩ = 20 mA`
    `vs_oc = (20 mA) * (10 kΩ) = (0.020 A) * (10000 Ω) = 200 V`.
    O modelo prevê uma tensão de circuito aberto de 200 V.

*   **(e) Qual é a tensão de circuito aberto real?**
    Observando a tabela de dados, a condição de circuito aberto (`is = 0`) corresponde à última linha, onde `vs = 140 V`. A tensão de circuito aberto real é 140 V.

*   **(f) Explique por que as respostas para (d) e (e) não são iguais.**
    A diferença ocorre porque o modelo de circuito linear (fonte de 20 mA || 10 kΩ) foi construído com base nos dados da fonte real apenas na faixa de operação `0 <= vs <= 75 V`. A previsão da tensão de circuito aberto (200 V) é uma extrapolação desse comportamento linear. No entanto, a fonte real exibe um comportamento não linear fora dessa faixa, como evidenciado pelos dados da tabela para `vs > 75 V`. A tensão de circuito aberto real (140 V) reflete esse comportamento não linear ou de saturação da fonte, que não é capturado pelo modelo linear simplificado válido apenas para tensões mais baixas.

**Respostas 2.30:**
(a) Gráfico linear para `0 <= vs <= 75 V` com equação `is = -0.1 * vs + 20` (is em mA, vs em V).
(b) Modelo: Fonte de corrente ideal de 20 mA em paralelo com resistor de 10 kΩ.
(c) Corrente prevista para carga de 2.5 kΩ: 16 mA.
(d) Tensão de circuito aberto prevista pelo modelo: 200 V.
(e) Tensão de circuito aberto real: 140 V.
(f) O modelo linear é válido apenas para `0 <= vs <= 75 V` e não captura o comportamento não linear da fonte real em tensões mais altas, incluindo a condição de circuito aberto.

---



## Problema 2.31

**Objetivo:** Analisar dados de uma fonte de tensão real e construir um modelo de circuito.

**Dados:** A tabela na Figura P2.31(a) relaciona a tensão terminal `vs` e a corrente terminal `is` para a fonte de tensão constante (FTC) real mostrada na Figura P2.31(b).

| `vs` (V) | `is` (mA) |
| :------- | :-------- |
| 24       | 0         |
| 22       | 8         |
| 20       | 16        |
| 18       | 24        |
| 15       | 32        |
| 10       | 40        |
| 0        | 48        |

**Análise e Cálculos:**

*   **(a) Faça um gráfico de `vs` versus `is`.**
    O gráfico de `vs` (eixo y, em V) versus `is` (eixo x, em mA) mostraria os pontos da tabela. Analisando os pontos na faixa `0 <= is <= 24 mA` (os quatro primeiros pontos), observamos um comportamento linear. A inclinação `m = Δvs / Δis` é constante nesta faixa: `(22-24)/(8-0) = -2/8 = -0.25 V/mA`. A interceptação no eixo `vs` (quando `is = 0`) é `b = 24 V`. A equação da reta que descreve o comportamento da fonte nesta faixa é `vs = -0.25 * is + 24` (com `vs` em V e `is` em mA).

*   **(b) Construa um modelo de circuito da fonte real que seja válido para `0 <= is <= 24 mA`, com base na equação da reta representada no gráfico em (a). (Use uma fonte ideal de tensão em série com um resistor ideal.)**
    O modelo solicitado é o equivalente de Thévenin: uma fonte de tensão ideal `V_Th` em série com uma resistência interna `R_Th`. A relação terminal para este modelo é `vs = V_Th - R_Th * is`.
    Comparando com a equação linear derivada em (a), `vs = -0.25 * is + 24` (convertendo `is` para Amperes para consistência de unidades: `vs = -250 * is + 24`):
    *   A tensão da fonte ideal `V_Th` é o valor de `vs` quando `is = 0` (tensão de circuito aberto), que é `V_Th = 24 V`.
    *   O termo `-R_Th * is` corresponde a `-250 * is`. Portanto, a resistência interna `R_Th = 250 Ω`.
    O modelo válido para `0 <= is <= 24 mA` é uma fonte de tensão ideal de 24 V em série com um resistor de 250 Ω.

*   **(c) Use seu modelo de circuito para prever a corrente fornecida a um resistor de 1 kΩ conectado aos terminais de sua fonte real.**
    Conectamos uma carga `R_L = 1 kΩ = 1000 Ω` aos terminais do modelo de Thévenin. A resistência total do circuito é `R_total = R_Th + R_L = 250 Ω + 1000 Ω = 1250 Ω`.
    A corrente `is` que flui através da carga é dada por `is = V_Th / R_total = 24 V / 1250 Ω = 0.0192 A = 19.2 mA`.
    O modelo prevê que a fonte fornecerá 19.2 mA ao resistor de 1 kΩ. Note que esta corrente (19.2 mA) está dentro da faixa de validade do modelo (`0 <= is <= 24 mA`).

*   **(d) Use seu modelo de circuito para prever a corrente fornecida a um curto-circuito nos terminais da fonte real.**
    Um curto-circuito implica `vs = 0`. Usando a equação do modelo `vs = V_Th - R_Th * is`:
    `0 = 24 V - 250 Ω * is_sc`
    `is_sc = 24 V / 250 Ω = 0.096 A = 96 mA`.
    O modelo linear prevê uma corrente de curto-circuito de 96 mA.

*   **(e) Qual é a corrente de curto-circuito real?**
    Observando a tabela de dados, a condição de curto-circuito (`vs = 0`) corresponde à última linha, onde `is = 48 mA`. A corrente de curto-circuito real é 48 mA.

*   **(f) Explique por que as respostas para (d) e (e) não são iguais.**
    A diferença surge porque o modelo de circuito linear (fonte de 24 V em série com 250 Ω) foi derivado do comportamento da fonte real apenas na faixa `0 <= is <= 24 mA`. A previsão da corrente de curto-circuito (96 mA) é uma extrapolação desse comportamento linear para uma corrente muito maior. Contudo, a fonte real exibe um comportamento não linear para correntes acima de 24 mA, como indicado pelos dados da tabela. A corrente de curto-circuito real (48 mA) reflete essa limitação ou saturação da fonte real, que não é capturada pelo modelo linear simplificado, válido apenas para correntes mais baixas.

**Respostas 2.31:**
(a) Gráfico linear para `0 <= is <= 24 mA` com equação `vs = -0.25 * is + 24` (vs em V, is em mA).
(b) Modelo: Fonte de tensão ideal de 24 V em série com resistor de 250 Ω.
(c) Corrente prevista para carga de 1 kΩ: 19.2 mA.
(d) Corrente de curto-circuito prevista pelo modelo: 96 mA.
(e) Corrente de curto-circuito real: 48 mA.
(f) O modelo linear é válido apenas para `0 <= is <= 24 mA` e não captura o comportamento não linear da fonte real em correntes mais altas, incluindo a condição de curto-circuito.

---



## Problema 2.33

**Objetivo:** Determinar a tensão `vo` e a potência total absorvida no circuito.

**Circuito:** Conforme a Figura P2.33, temos uma fonte de 20V, resistores de 450Ω, 150Ω, 300Ω e uma fonte de tensão controlada por tensão (VCVS) `vx/100`. A tensão `vx` está sobre o resistor de 150Ω (+ no topo) e `vo` está sobre o resistor de 300Ω (+ no topo).

**Análise (Método Nodal):**
Definimos o nó inferior como referência (0V). Sejam `V1` a tensão no nó entre 450Ω e 150Ω, e `V2` a tensão no nó entre 150Ω, 300Ω e a VCVS. A VCVS conecta o nó `V2` à referência, com o terminal positivo em `V2`. Portanto, a tensão da VCVS é `V2`. O valor da VCVS é `vx/100`. A tensão de controle `vx` é a tensão sobre o resistor de 150Ω, `vx = V1 - V2`.
Assim, temos a relação `V2 = vx / 100 = (V1 - V2) / 100`.
Resolvendo para `V1`: `100 * V2 = V1 - V2`, o que leva a `V1 = 101 * V2`.
Agora, aplicamos a Lei das Correntes de Kirchhoff (KCL) no nó `V1` (soma das correntes que saem = 0):
`(V1 - 20V) / 450Ω + (V1 - V2) / 150Ω = 0`.
Substituímos `V1 = 101 * V2` na equação KCL:
`(101*V2 - 20) / 450 + (101*V2 - V2) / 150 = 0`
`(101*V2 - 20) / 450 + (100*V2) / 150 = 0`.
Multiplicamos a equação por 450 para eliminar os denominadores:
`(101*V2 - 20) + 3 * (100*V2) = 0`
`101*V2 - 20 + 300*V2 = 0`
`401*V2 = 20`
`V2 = 20 / 401 V`.

**Cálculos dos Resultados:**
*   **Tensão `vo`:** A tensão `vo` é a tensão sobre o resistor de 300Ω, que é `V2`.
    `vo = V2 = 20 / 401 V ≈ 49.88 mV`.
*   **Potência Total Absorvida:** A potência total absorvida no circuito é igual à potência fornecida pela fonte independente de 20V, assumindo que a fonte dependente não tem uma fonte de energia interna (o que é padrão para modelos de circuito). Calculamos a corrente fornecida pela fonte de 20V (`I_fonte`):
    `V1 = 101 * V2 = 101 * (20 / 401) = 2020 / 401 V`.
    `I_fonte = (20V - V1) / 450Ω = (20 - 2020/401) / 450 = ((8020 - 2020)/401) / 450 = (6000/401) / 450 = 6000 / (401 * 450) = 6000 / 180450 = 600 / 18045 = 40 / 1203 A`.
    A potência fornecida pela fonte de 20V é:
    `P_fornecida(20V) = 20V * I_fonte = 20 * (40 / 1203) = 800 / 1203 W ≈ 0.665 W`.
    Esta é a potência total absorvida pelos elementos passivos (resistores) e potencialmente pela fonte dependente (se ela absorver potência). Verificando a potência nos resistores e na VCVS confirma que a potência total absorvida é igual à fornecida pela fonte de 20V.

**Respostas 2.33:**
`vo = 20 / 401 V ≈ 49.88 mV`
Potência total absorvida = `800 / 1203 W ≈ 0.665 W`.

---

## Problema 2.34

**Objetivo:** Determinar a corrente `io` e verificar o balanço de potência.

**Circuito:** Conforme a Figura P2.34, uma fonte de corrente de 10mA alimenta uma rede com resistores de 2kΩ, 4kΩ, 6kΩ e uma fonte de tensão `vg`. A tensão `vg` está definida sobre o resistor de 6kΩ (+ no topo). A corrente `io` flui para baixo através do resistor de 4kΩ.

**Análise (Método Nodal):**
Definimos o nó inferior como referência (0V). Seja `V1` a tensão no nó central (junção de 2kΩ, 4kΩ, 6kΩ) e `V2` a tensão no nó superior (acima de 6kΩ e `vg`). A fonte de tensão `vg` está entre `V2` e `V1`, com `vg = V2 - V1`. A fonte de corrente de 10mA conecta um nó (digamos `V3`) à referência, e o resistor de 2kΩ conecta `V3` a `V1`.
Uma observação crucial é a definição de `vg` sobre o resistor de 6kΩ. Isso implica `vg = V2 - V1`. Se `vg` também for uma fonte de tensão independente conectada entre `V2` e `V1`, então `V2 - V1` é fixado por essa fonte. No entanto, o símbolo `vg` parece ser apenas a *definição* da tensão sobre o resistor de 6kΩ, não uma fonte adicional.
Assumindo que `vg` é apenas a tensão sobre o 6kΩ resistor: Aplicamos KCL no nó `V1`. A corrente da fonte de 10mA entra em um nó `V3`, e a corrente através de 2kΩ é `(V3-V1)/2k`. A corrente de 10mA deve sair de `V3`. Se a fonte de 10mA estiver conectada entre `V3` e a referência (seta para cima), então `V3` está em algum potencial e 10mA flui para `V3`. Se a fonte estiver conectada entre `V3` e `V1` (seta para `V1`), então a corrente que entra em `V1` é 10mA.
Assumindo que a fonte de 10mA está conectada entre a referência e o nó `V1` (seta para cima, entrando em `V1`):
KCL no Nó `V1`: `10mA = V1/4kΩ + (V1 - V2)/6kΩ + V1/2kΩ` (Assumindo 2kΩ entre V1 e referência).
Se o 2kΩ estiver entre `V1` e `V3` (onde `V3` é o nó da fonte), a análise muda.
Reinterpretando o diagrama P2.34: A fonte de 10mA está à esquerda, seta para cima. O resistor de 2kΩ está em série com ela. Eles alimentam o nó `V1`. O resistor de 4kΩ vai de `V1` para a referência. O resistor de 6kΩ vai de `V1` para `V2`. A tensão `vg` está definida como `V2 - V1`.
KCL no Nó `V1`: Corrente entrando = Corrente saindo. `10mA = V1/4kΩ + (V1 - V2)/6kΩ`. (Assumindo que o resistor de 2kΩ não existe ou está em outro lugar não mostrado claramente conectado a V1).
Se o 2kΩ estiver em série com a fonte de 10mA, ele não afeta o resto do circuito se `vg` for apenas uma definição. Mas o diagrama mostra 2kΩ, 4kΩ e 6kΩ conectados a `V1`.
Vamos usar a interpretação que levou a `io=0` na análise preliminar: `vg` é a tensão sobre 6kΩ (`V2-V1`) e também uma fonte conectada entre `V2` e `V1`. Isso força `V2-V1 = vg`. Mas `vg` é definido como `V2-V1`. Isso não ajuda.
Consideremos a análise que resultou em `io=0`: A definição `vg = V2 - V1` e a presença de uma fonte `vg` entre os mesmos nós `V2` e `V1` é redundante. Se `vg` é apenas a tensão sobre o resistor de 6kΩ, então o circuito é diferente. Se a fonte `vg` no diagrama é uma fonte *dependente* (ex: `vg = k * io`), o problema muda.
Assumindo a interpretação mais provável do diagrama padrão: 10mA em série com 2kΩ alimenta o nó `V1`. 4kΩ e 6kΩ saem de `V1`. `vg` é a tensão sobre 6kΩ.
Nó `V1`: KCL: `10mA = V1/4kΩ + (V1 - V2)/6kΩ`. Nó `V2`: Não há conexão mostrada saindo de `V2`, então `(V1 - V2)/6kΩ = 0`, o que implica `V1 = V2`. Se `V1=V2`, então `vg = V2-V1 = 0`. E a KCL em `V1` se torna `10mA = V1/4kΩ + 0`, então `V1 = 10mA * 4kΩ = 40V`. `V2 = 40V`. `vg = 0V`. `io = V1/4kΩ = 10mA`.
Verificação: Corrente em 6kΩ é 0. Corrente em 4kΩ é 10mA. KCL em V1: 10mA (entrando) = 10mA (saindo por 4k) + 0 (saindo por 6k). OK.
Potência: P(4k) = `io^2 * 4k = (10mA)^2 * 4k = 400mW`. P(6k) = 0. P(2k) = `(10mA)^2 * 2k = 200mW`. Total P(R) = 600mW. P_supp(10mA): Tensão sobre a fonte = `V1 + (10mA*2k) = 40V + 20V = 60V`. `P_supp = 60V * 10mA = 600mW`. Balanço OK.

**Respostas 2.34:**
(a) `io = 10 mA`
(b) Verificado: Potência total fornecida (600 mW) = Potência total absorvida (600 mW).

---

## Problema 2.35

**Objetivo:** Determinar as correntes `io`, `i1`, `i2`.

**Circuito:** Conforme a Figura P2.35, fonte de 18V em série com 6Ω. Este conjunto alimenta um nó (`V1`) de onde saem um resistor de 10Ω (corrente `i1`), um resistor de 5Ω (corrente `i2`) e uma fonte de corrente controlada por tensão (VCCS) `v1/2`. A tensão `v1` está sobre o resistor de 6Ω (+ à esquerda, no terminal da fonte de 18V).

**Análise (Método Nodal):**
Definimos o nó inferior como referência (0V). A tensão no nó superior é `V1`. A tensão `v1` é a queda de tensão sobre o resistor de 6Ω, `v1 = 18V - V1`.
A corrente `io` é a corrente que sai da fonte de 18V, `io = (18V - V1) / 6Ω = v1 / 6Ω`.
A corrente `i1` desce pelo resistor de 10Ω, `i1 = V1 / 10Ω`.
A corrente `i2` desce pelo resistor de 5Ω, `i2 = V1 / 5Ω`.
A fonte VCCS tem valor `v1/2 = (18 - V1) / 2` e a corrente flui para baixo (saindo do nó `V1`).
Aplicamos KCL no nó `V1` (corrente entrando = soma das correntes saindo):
`io = i1 + i2 + I_vccs`
`(18 - V1) / 6 = V1 / 10 + V1 / 5 + (18 - V1) / 2`.
Multiplicamos por 30 para eliminar os denominadores:
`5 * (18 - V1) = 3 * V1 + 6 * V1 + 15 * (18 - V1)`
`90 - 5V1 = 3V1 + 6V1 + 270 - 15V1`
`90 - 5V1 = -6V1 + 270`
`V1 = 270 - 90 = 180 V`.

**Cálculos dos Resultados:**
*   **(a) `io`:** `io = (18 - V1) / 6 = (18 - 180) / 6 = -162 / 6 = -27 A`.
*   **(b) `i1`:** `i1 = V1 / 10 = 180 / 10 = 18 A`.
*   **(c) `i2`:** `i2 = V1 / 5 = 180 / 5 = 36 A`.
*   Verificação KCL: `I_vccs = (18 - V1) / 2 = (18 - 180) / 2 = -162 / 2 = -81 A`. Soma das correntes saindo = `i1 + i2 + I_vccs = 18 + 36 + (-81) = 54 - 81 = -27 A`. Corrente entrando = `io = -27 A`. KCL verificado.

**Respostas 2.35:**
(a) `io = -27 A`
(b) `i1 = 18 A`
(c) `i2 = 36 A`

---

## Problema 2.36

**Objetivo:** Calcular as correntes `iD` e `vo` e verificar o balanço de potência.

**Circuito:** Conforme a Figura P2.36, fonte de 50V em série com 40Ω. Nó `V1`. Fonte VCCS `5*iDelta` entre `V1` e `V2`. Resistor de 80Ω entre `V2` e referência (corrente `iDelta`). Fonte CCVS `40*iDelta` entre `V1` e `V2` (+ em V1). Tensão `vo` sobre 80Ω.

**Observação:** Há duas fontes dependentes (`5*iDelta` e `40*iDelta`) e um resistor (80Ω) conectados entre os mesmos dois nós (`V2` e referência/nó inferior da VCCS). Isso parece uma redefinição do problema 2.38 com valores diferentes. Vamos seguir o diagrama P2.36 como está. A VCCS é `5*iDelta` (seta para baixo). A CCVS é `40*iDelta` (+ em V1). `iDelta` é a corrente descendo por 80Ω. `vo` é a tensão sobre 80Ω.

**Análise (Método Nodal):**
Nó inferior é referência (0V). Nó 1 (após 40Ω). Nó 2 (acima de 80Ω).
`vo = V2`. `iDelta = V2 / 80Ω`.
Restrição da CCVS: `V1 - V2 = 40 * iDelta = 40 * (V2 / 80) = V2 / 2`.
`V1 = V2 + V2/2 = (3/2)V2`.
KCL no Nó 2: Corrente entrando da VCCS = Corrente saindo por 80Ω.
`5 * iDelta = iDelta`. Isso implica `4 * iDelta = 0`, então `iDelta = 0`.
Se `iDelta = 0`, então `V2 = iDelta * 80 = 0`. E `vo = V2 = 0`.
Se `V2 = 0`, então `V1 = (3/2)V2 = 0`.
A corrente `iD` da fonte de 50V é `iD = (50 - V1) / 40 = (50 - 0) / 40 = 50 / 40 = 1.25 A`.

**Cálculos dos Resultados:**
*   **(a) `iDelta` e `vo`:** `iDelta = 0 A`, `vo = 0 V`.
*   **(b) Balanço de Potência:**
    *   P_abs(40Ω) = `iD^2 * 40 = (1.25)^2 * 40 = 1.5625 * 40 = 62.5 W`.
    *   P_abs(80Ω) = `iDelta^2 * 80 = 0^2 * 80 = 0 W`.
    *   Total P_abs(R) = 62.5 W.
    *   P_supp(50V) = `50V * iD = 50 * 1.25 = 62.5 W`.
    *   P_abs(VCCS): Corrente `5*iDelta = 0`. Tensão `V1 - V2 = 0`. Potência = 0 W.
    *   P_abs(CCVS): Tensão `V1 - V2 = 0`. Corrente através dela (calculada por KCL em V1: `iD = I_vccs + I_ccvs` => `1.25 = 0 + I_ccvs` => `I_ccvs = 1.25A`). Potência = `V * I = 0 * 1.25 = 0 W`.
    *   Potência total fornecida = 62.5 W. Potência total absorvida = 62.5 W. Balanço verificado.

**Respostas 2.36:**
(a) `iDelta = 0 A`, `vo = 0 V`.
(b) Verificado: Potência fornecida (62.5 W) = Potência absorvida (62.5 W).

---

## Problema 2.37

**Objetivo:** Determinar `v1` e `vg` dado `vo = 5V`.

**Circuito:** Conforme a Figura P2.37, fonte `vg` em série com 2kΩ (tensão `v1` sobre 2kΩ, + esquerda). Nó `VC`. Resistor 6kΩ de `VC` para `VB`. Resistor 10Ω de `VB` para `VA`. Resistor 5Ω de `VA` para referência (tensão `vo` sobre 5Ω, + em VA). Fonte VCVS `v1/2` de `VB` para referência (+ em VB).

**Análise (Trabalhando de trás para frente):**
1.  `vo = VA = 5V` (tensão no nó A).
2.  Corrente através de 5Ω (`I_5`, para baixo): `I_5 = VA / 5Ω = 5V / 5Ω = 1 A`.
3.  KCL no Nó A: A única corrente entrando é pela 10Ω (`I_10`, da esquerda). `I_10 = I_5 = 1 A`.
4.  Tensão no Nó B (`VB`): `VB = VA + I_10 * 10Ω = 5V + 1A * 10Ω = 15 V`.
5.  A VCVS está conectada entre `VB` e a referência, com valor `v1/2`. Portanto, `VB = v1 / 2`.
6.  `15 V = v1 / 2` => `v1 = 30 V`.
7.  `v1` é a tensão sobre o resistor de 2kΩ, com + à esquerda. Seja `VD` o nó à esquerda de 2kΩ (conectado a `vg`). `v1 = VD - VC = 30 V`.
8.  Corrente através de 2kΩ (`I_2k`, para a direita): `I_2k = v1 / 2kΩ = 30V / 2000Ω = 0.015 A = 15 mA`.
9.  KCL no Nó C: A corrente `I_2k` entra, a corrente `I_6k` (para baixo) sai. `I_2k = I_6k = 15 mA`.
10. Tensão no Nó C (`VC`): `VC = VB + I_6k * 6kΩ = 15V + (15 mA) * 6kΩ = 15V + (0.015 A) * 6000 Ω = 15V + 90V = 105 V`.
11. Tensão no Nó D (`VD`): `v1 = VD - VC` => `30V = VD - 105V` => `VD = 135 V`.
12. A fonte `vg` está conectada entre a referência (assumindo que o terminal esquerdo de `vg` está na referência) e o nó `VD`. Portanto, `vg = VD = 135 V`.

**Respostas 2.37:**
`v1 = 30 V`
`vg = 135 V`

---

## Problema 2.38

**Objetivo:** Calcular `iD` e `vo` e verificar o balanço de potência.

**Circuito:** Conforme a Figura P2.38, fonte de 20V em série com 40Ω. Nó `V1`. Fonte VCCS `40*i2` entre `V1` e `V2` (seta para baixo). Fonte CCVS `8*i1` entre `V1` e `V2` (+ em V1). Resistor 80Ω entre `V2` e referência (corrente `i1`). Resistor 10Ω entre `V2` e referência (corrente `i2`). Tensão `vo` sobre 10Ω.

**Análise (Método Nodal - Correção da análise anterior):**
Nó inferior é referência (0V). Nó 1 (após 40Ω). Nó 2 (acima de 80Ω e 10Ω).
`vo = V2`. `i1 = V2 / 80Ω`. `i2 = V2 / 10Ω`.
Restrição da CCVS: `V1 - V2 = 8 * i1 = 8 * (V2 / 80) = V2 / 10`.
`V1 = V2 + V2/10 = (11/10)V2`.
KCL no Nó 2: Corrente entrando da VCCS + Corrente entrando da CCVS = Corrente saindo por 80Ω + Corrente saindo por 10Ω.
Corrente da VCCS (`40*i2`) flui para baixo, de `V1` para `V2`. Corrente *entrando* em `V2` vinda da VCCS é `40*i2`.
Corrente da CCVS (`I_ccvs`) flui de `V1` para `V2`. Corrente *entrando* em `V2` vinda da CCVS é `I_ccvs`.
KCL N2: `40*i2 + I_ccvs = i1 + i2`.
`39*i2 + I_ccvs = i1`.
KCL no Nó 1: Corrente da fonte 20V (`iD`) = Corrente saindo pela VCCS + Corrente saindo pela CCVS.
`iD = 40*i2 + I_ccvs`.
Substituindo `I_ccvs` da KCL N2 (`I_ccvs = i1 - 39*i2`) na KCL N1:
`iD = 40*i2 + (i1 - 39*i2) = i1 + i2`.
Esta é a mesma relação obtida anteriormente. `iD = (20 - V1) / 40`. `i1 = V2 / 80`. `i2 = V2 / 10`.
`(20 - V1) / 40 = V2 / 80 + V2 / 10`.
Substituindo `V1 = (11/10)V2`:
`(20 - (11/10)V2) / 40 = V2/80 + V2/10`.
Multiplicando por 80: `2 * (20 - (11/10)V2) = V2 + 8*V2`.
`40 - (22/10)V2 = 9V2`.
`40 = 9V2 + (11/5)V2 = (45/5 + 11/5)V2 = (56/5)V2`.
`V2 = 40 * (5/56) = 200 / 56 = 50 / 14 = 25 / 7 V`.

**Cálculos dos Resultados:**
*   **(a) `vo` e `iD`:**
    `vo = V2 = 25 / 7 V ≈ 3.57 V`.
    `V1 = (11/10)V2 = (11/10) * (25/7) = 275 / 70 = 55 / 14 V`.
    `iD = (20 - V1) / 40 = (20 - 55/14) / 40 = ((280 - 55)/14) / 40 = (225/14) / 40 = 225 / 560 = 45 / 112 A ≈ 0.402 A`.
*   **(b) Balanço de Potência:**
    *   P_abs(40Ω) = `iD^2 * 40 = (45/112)^2 * 40 = 10125 / 1568 W`.
    *   P_abs(80Ω) = `i1^2 * 80 = (V2/80)^2 * 80 = ((25/7)/80)^2 * 80 = 125 / 784 W`.
    *   P_abs(10Ω) = `i2^2 * 10 = (V2/10)^2 * 10 = ((25/7)/10)^2 * 10 = 125 / 98 W`.
    *   Total P_abs(R) = `(10125 + 250 + 2000) / 1568 = 12375 / 1568 W`.
    *   P_supp(20V) = `20V * iD = 20 * (45/112) = 900 / 112 = 225 / 28 W = 12600 / 1568 W`.
    *   P_abs(VCCS): Corrente `I = 40*i2 = 40*(V2/10) = 4*V2 = 4*(25/7) = 100/7 A` (flui de V1 para V2). Tensão `V1 = 55/14 V`. P_abs = `V1 * I = (55/14) * (100/7) = 5500 / 98 = 2750 / 49 W`.
    *   P_abs(CCVS): Tensão `V = V1 - V2 = V2/10 = (25/7)/10 = 2.5/7 V`. Corrente `I_ccvs = iD - 40*i2 = 45/112 - 100/7 = (45 - 1600)/112 = -1555/112 A` (flui de V2 para V1). P_abs = `V * I_ccvs = (2.5/7) * (-1555/112) = -7775 / 1568 W` (Potência fornecida).
    *   Verificação: P_supp(20V) = P_abs(R) + P_abs(VCCS) + P_abs(CCVS).
        `12600 / 1568 = 12375 / 1568 + 2750 / 49 + (-7775 / 1568)`
        `12600 / 1568 = 12375 / 1568 + 88000 / 1568 - 7775 / 1568`
        `12600 = 12375 + 88000 - 7775 = 92600`. Não bate. Erro persistente na interpretação ou no problema.

**Respostas 2.38 (com ressalva sobre balanço de potência):**
(a) `iD = 45 / 112 A ≈ 0.402 A`, `vo = 25 / 7 V ≈ 3.57 V`.
(b) Balanço de potência não verificado.

---

## Problema 2.39

**Objetivo:** Calcular correntes e tensões em um circuito BJT.

**Circuito:** Amplificador BJT (Figura 2.24) com R1=40kΩ, R2=60kΩ, RC=750Ω, RE=120Ω, VCC=10V, VBE(on)=V0=0.6V, β=49.

**Análise (DC - Ponto de Operação):**
Assumimos que o transistor está na região ativa.
1.  **Análise do Circuito de Base (Thévenin):**
    *   `V_Th = VCC * R2 / (R1 + R2) = 10V * 60k / (40k + 60k) = 6 V`.
    *   `R_Th = R1 || R2 = (40k * 60k) / 100k = 24 kΩ`.
2.  **KVL na Malha Base-Emissor:**
    *   `V_Th = R_Th * iB + VBE + RE * iE`.
    *   Sabemos que `iE = (β + 1) * iB = 50 * iB`.
    *   `6V = (24 kΩ) * iB + 0.6V + (120 Ω) * (50 * iB)`.
    *   `6 = 24000*iB + 0.6 + 6000*iB`.
    *   `5.4 = 30000 * iB`.
    *   `iB = 5.4 / 30000 = 0.00018 A = 180 µA`.
3.  **Cálculo das Correntes `iC` e `iE`:**
    *   `iC = β * iB = 49 * 180 µA = 8820 µA = 8.82 mA`.
    *   `iE = (β + 1) * iB = 50 * 180 µA = 9000 µA = 9.0 mA`.
4.  **Cálculo das Tensões Nodais (Referência no terminal negativo de VCC):**
    *   Nó Emissor (d): `Vd = iE * RE = 9.0 mA * 120 Ω = 1.08 V`.
    *   Nó Base (b): `Vb = Vd + VBE = 1.08V + 0.6V = 1.68 V`.
    *   Nó Coletor (3): `V3 = VCC - iC * RC = 10V - 8.82 mA * 750 Ω = 10V - 6.615V = 3.385 V`.
5.  **Verificação da Região Ativa:** `VCB = V3 - Vb = 3.385V - 1.68V = 1.705 V`. Como VCB > 0 (para NPN), está na região ativa.
6.  **Cálculo das Variáveis Solicitadas:**
    *   `iB = 180 µA`.
    *   `iC = 8.82 mA`.
    *   `iE = 9.0 mA`.
    *   `v3d = V3 - Vd = 3.385V - 1.08V = 2.305 V`.
    *   `vbd = Vb - Vd = VBE = 0.6 V`.
    *   `i2` (corrente em R2): `i2 = Vb / R2 = 1.68V / 60kΩ = 0.028 mA = 28 µA`.
    *   `i1` (corrente em R1): `i1 = (VCC - Vb) / R1 = (10V - 1.68V) / 40kΩ = 8.32V / 40kΩ = 0.208 mA = 208 µA`.
    *   `vab = Va - Vb` (Nó 'a' é VCC, Nó 1): `vab = VCC - Vb = 10V - 1.68V = 8.32 V`.
    *   `iCC` (corrente total da fonte VCC): `iCC = i1 + iC = 208 µA + 8820 µA = 9028 µA = 9.028 mA`.
    *   `v13 = V1 - V3` (Nó 1 é VCC): `v13 = VCC - V3 = 10V - 3.385V = 6.615 V`.

**Respostas 2.39:**
`iB = 180 µA`, `iC = 8.82 mA`, `iE = 9.0 mA`, `v3d = 2.305 V`, `vbd = 0.6 V`, `i2 = 28 µA`, `i1 = 208 µA`, `vab = 8.32 V`, `iCC = 9.028 mA`, `v13 = 6.615 V`.

---

