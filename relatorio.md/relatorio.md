# 1 Introdução

Uma fonte de alimentação é um circuito responsável por fornecer energia elétrica adequada para dispositivos eletrônicos.

Neste projeto foi desenvolvido um circuito capaz de converter tensão alternada (AC) em tensão contínua (DC) regulada de 12V utilizando uma ponte retificadora e o regulador de tensão 7812.

# 2 Funcionamento do Circuito

O funcionamento do circuito ocorre em quatro etapas:

1. Entrada da tensão AC
2. Retificação
3. Filtragem
4. Regulação da tensão

# 3 Descrição dos Componentes

## J1 – Conector de Entrada

Responsável pela entrada da tensão alternada.

Pinos:

Pino 1 → AC  
Pino 2 → AC

Essa tensão geralmente vem de um transformador.

## BR1 – Ponte Retificadora

A ponte retificadora converte a tensão AC em tensão DC pulsante.

Ela possui:

Entradas:

AC1  
AC2  

Saídas:

Positivo (+)  
Negativo (GND)

## C1 – Capacitor de Filtragem (1000µF)

Após a retificação a tensão ainda possui ondulações chamadas ripple.

O capacitor C1 reduz essas ondulações armazenando energia e liberando gradualmente.

## C2 – Capacitor de Desacoplamento (100nF)

Este capacitor remove ruídos de alta frequência presentes na linha de alimentação antes do regulador.

## U1 – Regulador de Tensão 7812

O CI 7812 é responsável por estabilizar a tensão de saída em 12V.

Pinagem:

Pino 1 – Entrada (VI)  
Recebe a tensão DC filtrada.

Pino 2 – Terra (GND)  
Referência do circuito.

Pino 3 – Saída (VO)  
Fornece tensão regulada de 12V.

## C3 – Capacitor de Saída (100nF)

Utilizado para estabilizar a saída do regulador e evitar oscilações.

## R1 – Resistor (100Ω)

Limita a corrente que passa pelo LED indicador.

Sem ele o LED poderia queimar.

## D1 – LED

Indica visualmente que a fonte está energizada.

Pinos:

Anodo (A) → ligado ao resistor  
Catodo (K) → ligado ao GND

## J2 – Conector de Saída

Conector responsável por fornecer a tensão regulada.

Pinos:

Pino 1 → 12V  
Pino 2 → GND

# 4 Fluxo da Energia no Circuito

A energia percorre o seguinte caminho:

AC → J1  
↓  
Ponte retificadora BR1  
↓  
Capacitor de filtro C1  
↓  
Regulador 7812  
↓  
Capacitor de saída C3  
↓  
Saída estabilizada em J2

# 5 Conclusão

O circuito desenvolvido fornece uma tensão estável de 12V DC a partir de uma entrada AC.

Esse tipo de fonte é simples, confiável e muito utilizado em projetos eletrônicos de pequeno porte.