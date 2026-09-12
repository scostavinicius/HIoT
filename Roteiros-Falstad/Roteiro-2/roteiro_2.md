# EXPERIMENTO 01: Polarização direta versus Polarização reversa de Diodos.

![Figura 1 - Circuito de polarização direta.](imagens/figura1-polarizacao-direta.png)

*Figura 1 - Circuito de polarização direta.*

1. Monte o circuito da Figura 1, ligue a fonte de tensão e observe o comportamento do LED. Envie o arquivo da simulação como um link Falstad (*Circuit Simulator Falstad → Arquivo → Exportar como Link*). Qual o comportamento do LED?

    [Circuito 1](https://www.falstad.com/circuit/circuitjs.html?ctz=DwYwlgTgBAZgvAIgIwKgFwM6IAwDpsEECsqYIiAzABwBMuA7AGw1G1IAsFAnF9o+6hAAjREWyoADiISdUANwijUAW0yiApgFokKAHwAoKFGAATKAA9E7KlGtQujW1VTwE4qMoD2iE+pgBDAFcAGzQEAHoDI2AAGQBRABELRCRGbCgkJgy0jK4aFxwVbwRfAJC0TWD1E0FFZEEAc0KoYWblIXI3fBRIw2MAd2TkHKQ87PSaGgFYQt7o6Eth9Kp01NWaZxm3VDqkQgiogaG1jI3xjKYC7bmjxYcnc+sr8RvgQcWTyfYobUcv54OfTexxydhOKwBr3eiF+DzsTy2L0OwDkQ1hXx+qScV1SqH6rncyn85jkSigkBw+GwPQMwHC4AgBiAA)

    **Resposta:** O LED fica constantemente ligado

2. Meça a tensão em cima do resistor de 1k. Qual o valor encontrado? Explique o porquê da tensão ser menor que 5V.

    **Resposta:** Os diodos consomem uma parcela fixa de tensão, o que diminue a tensão restante para o resistor.

3. Calcule a corrente que passa pelo resistor 1k considerando que o LED vermelho opera em nível de tensão de 1,7V e o diodo com 0,7V. O valor calculado é igual ao medido no circuito simulado? Explique.

    **Resposta:**

    Considerando $V_{r}$ como a tensão no resistor, temos que:

    $$
    V_{r} = V_{fonte} - V_{diodo} - V_{LED}
    = 5 - 0{,}7 - 1{,}7
    = 2{,}6 
    $$

    Na simulação, foi medido a tensão de $2{,}835V$. O valor calculado é ligeiramente diferente do simulado. Isso acontece provavelmente porque o diodo e o LED do simulador devem operar em um diferente nível de tensão. 

![Figura 2 - Circuito de polarização reversa.](imagens/figura2-polarizacao-reversa.png)

*Figura 2 - Circuito de polarização reversa.*

1. Monte o circuito da Figura 2, ligue a fonte de tensão e observe o comportamento do LED. Envie o arquivo da simulação como um link Falstad (*Circuit Simulator Falstad → Arquivo → Exportar como Link*). Qual o comportamento do LED?

    [Circuito 2](https://www.falstad.com/circuit/circuitjs.html?ctz=DwYwlgTgBAZgvAIgIwKgFwM6IAwDpsEECsqYIiAzABwBMuA7AGw1G1IAsFAnF9o+6hAAjREWyoADiISdUANwijUAW0yiApgFokKAHwAoKFGByoAD0QtGUdlShX7NAbERJGqAO7wE4qMoCGZnJKUJA4+NgoAPQGRsAe5pZE1rZQFDTYNlSo3uIxhsYJFjLpWTalVL65CPlxRYicNI7s9snNOTg1sYWJCBSMdqmNWR0+XQXxvcNINIOlSEyjed3A0MXDleVNM9kuY1CKyITjdVPzXE3DNE5LJ8YAMgCiACJn20xbUEgXt34A9ogACbqGD+ACuABs0JoIepAYJDigoCAAOadZHSXzKITkHz4aIrQG9dKZVL9Qa7ar-IEg8FQ8bAKLgCAGIA)

    **Resposta:** O LED fica desligado

2. De acordo com os comportamentos observados nos itens 1 e 4, qual é a diferença entre os dois circuitos de polarização?

    **Resposta:** O circuito da figura 1 permanece sempre ligado pois o diodo permite a pessagem da corrente. Na figura 2, por causa do diodo em polarização invertida, a corrente não consegue passar.

3. Refaça o circuito sem o diodo e observe o comportamento do LED sem o diodo. Houve alguma diferença? Qual o motivo?

    **Resposta:** O LED continua desligado. Isso ocorre porque o LED também é um diodo, então ele não permite a passagem de corrente.

![Figura 3 - Circuito de polarização direta com fonte de tensão CA.](imagens/figura3-polarizacao-direta-ca.png)

*Figura 3 - Circuito de polarização direta com fonte de tensão CA.*

1. Monte o circuito da Figura 3. Configure o gerador de sinais para gerar uma função senoidal de 5V de pico e frequência de 1Hz. Responda os seguintes itens:

    [Circuito 3](https://www.falstad.com/circuit/circuitjs.html?ctz=DwYwlgTgBAZgvAIgIwKgFwM6IAwDpsEECsqYIiAzABwBMuA7AGw1G1IAsFAnF9o+6hAAjREWyoADiISdUANwijUAW0yiApgFokKAHwAoKFGByoAD1E0qUGjXZQiVqOyqp4yRqgDu7lLEXIKgCGZnJKUJA4+NgoAPQGRsBe5pbWLg5cNM6usDgI8YbGyRYI9Nj26WX2VOK5COIFicWIVTZ2Dk62AnUNCUUpCPzY2VCtLm55jf0lrUhOs0wT9fl9wNAz5VA1o5tzOe61AUiEK4VJA7OZO-ZdS71nADIAogAiF7tM11BImXcqAPaIAAm6hgQQArgAbNCaSHqIGCI6CADmeSgwjRyiE5Hq+DiqyBAyIV3SQ2yfygykBCBBYKhaFOwFi4AgBiAA)

   a. O LED acende em algum momento? Com que frequência acontece?

   **Resposta:** O LED acende e depois apaga. Isso acontece uma vez a cada segundo. 

   b. O que acontece com a tensão no resistor 1k quando o sinal senoidal permanece no eixo da tensão negativa? Qual o motivo deste comportamento?

   **Resposta:** A tensão abaixa para valores extremamente pequenos. Isso ocorre porque quando o eixo de tensão está negativo, a corrente percorre o circuito no fluxo inverso e os diodos não permitem que a corrente flua nesse sentido.

# EXPERIMENTO 02: Portas lógicas com Diodos.

![Figura 4 - Simulação de porta lógica com Diodos.](imagens/figura4-porta-logica-1.png)

*Figura 4 - Simulação de porta lógica com Diodos.*

1. Monte o circuito da Figura 4. Envie o arquivo da simulação como um link Falstad (*Circuit Simulator Falstad → Arquivo → Exportar como Link*).

    [Circuito 4](https://www.falstad.com/circuit/circuitjs.html?ctz=DwYwlgTgBAZgvAIgIwKgFwM6IAwDpsEECsqYIiSRAnLkdUgBwDM2ALFVW1U6iAEaIi2VAAcBCVjygA3CINQBbTIICmAWiQoAfACgoUYABMoAD0SsGUJg1ZQqANis3U8BMKgKA9okMqYAQwBXABs0BAB6XX1gAHdTRAcnWyR7bCSXHAiogzizCUtrW0TCjLcsvQNjPIsoVnsixzrWUvcvHz8g0PLo3ITG+qgUtKaW7pz4-NqBxJHYTMiK2Im1ACYV2yZ7SzUazYZRhZ7lzRXagigdy1YCA+ylvMvamtX1p-25ssPxh7XbVmfflYtrdFr1kKkkoMIbNXMIvvcKI5CrUCs4PnC7gBlCYpSGPEro1DBMCZdAAC0QKzGCIQjwsaQ0SFO9JBRweJxRDI513csOpYNxTRRU2ahPhAHNjkzORcOQB2Fa8+ZYnH9Wx0+qjKByNz4bAoKDE0loCkIKnwgAyAFEACKqtLUU5DKD2dZatoIXwBEJoNTBFSGXg6g0gcWk-ikhR8ci6-X8+1QR1Qh2pVkGaB5Z1EaVZ1OE7UUQjxzMQ7NO6GasV3MEaFaWewK5MuhVpmnOhvltKu0V8+E1wEd2V15tUquLaTLAeNl5-CylFKoGJ8jz+EzSeQLYDhcAQXRAA)

2. A alteração das chaves SW1 e SW2 para a posição 2 (sinal de tensão 5 V) representa o nível lógico 1. O nível lógico 0 é representado pela posição 1 (sinal de 0 V) das chaves. Observando o comportamento da carga (o LED) no circuito da Figura 4, qual porta lógica o circuito representa?

    **Resposta:** Representa a porta lógica OR, já que basta um dos switchs estar no nível lógico 1 para  o led ligar.

![Figura 5 - Simulação de porta lógica com Diodos.](imagens/figura5-porta-logica-2.png)

*Figura 5 - Simulação de porta lógica com Diodos.*

1. Monte o circuito da Figura 5 e analise o comportamento. Envie o arquivo da simulação como um link Falstad (*Circuit Simulator Falstad → Arquivo → Exportar como Link*).

    [Circuito 5](https://www.falstad.com/circuit/circuitjs.html?ctz=DwYwlgTgBAZgvAIgIwKgFwM6IAwDpsEECsqYIiSRAnLkdUgBwDM2ALFVW1U6iAEaIi2VAAcBCVjygA3CINQBbTIICmAWiQoAfACgoUYAHcoAD0EA2bFCJIATNar2bt1PATCA9Lv3AAyqcRzBgZrOygAdiInO1ccVDl3fGwUKAAbMDj0AAtEFy89A2MzZAIQ9nMIqKhy2PcEfJ8iilKocyIKpBaohlrPbwN-YvLqqgr2qxrYTIS8AhT0zLQchDz+owCV4JGKpirJtz6C9eLbLbaK07LR3vq16Q3O7BDzqEvW9tqkc1RDA8UAQxM0nkUEgOCSKAahQ2rC+23h+ziUOA0GKu3sw1hFURdSgCUeh0aGxezlaW2cN2RABMNtRovYSTEpriFAB7RBUlQwf4AV1SaFuRyaJSe1lOUEeV2+zMJ0OKkSc4qoYW6lLWwqorFYYpCkp1aqOABkAKIAEQ2ysVIU12tVMsU7IQnO5fLQalSKipvHxvAA5pl+JkFHxyIlkoKicVxtUGFZwmwY8J7cjhfHtaxYxEmNjrsndMAPOAILogA)

2. A alteração das chaves SW1 e SW2 para a posição 2 representa o nível lógico 1. O nível lógico 0 é representado pela posição 1 das chaves. Observando o comportamento da carga (o LED) no circuito da Figura 4, qual porta lógica o circuito representa?

    **Resposta:** Representa a porta lógica AND, já que se faz necessário que ambos switchs estejam no nível lógico 1 para que o LED possa ser aceso.