# Fonte de Tensão Regulável 3v - 12v (100mA)

Objetivo:

Criar uma fonte de tensao variavel entre 3 e 12 volts com capacidade de 100mA;

// Montar diagrama da fonte e lista contendo os preço das peças

// MOntar diagrama esquematica no eagle

// PCB placa impressa onde os componentes deverao ser soldados

// Eagle gratuito

// necessário somente montar a protoboard

// video explicando o projeto enquanto o mesmo esta funcionando

// monstar o projeto no git]

// todos precisam estar presencialmente para a apresentacao do projeto

// eh necessário saber explicar o porque cada parte do projeto para demonstar dominio 


Como Fazer?

// Oficialmente utilizando uma protoboard

// só espeta na protoboard

// somente se funcionar na protoboard pode fazer a placa

// primeira etapa eh baixar a voltagem de entrada de 127v para 12, utilizando um transformador 127v -> 12v

// Retificação, utilizar ponte de diodos para retificar a corrente, eles peguam uma onda senoidal e a colocam em modulo
// frequencia de 60hz

// usar capacitor para fazer a filtragem da onda, para evitar que o robo em alum ommento venha a parar
//o capacitor fornecera energia para o circuito quando o circuito e si comecar a perder energia entre vales


//utilizar, para concluir, ym regulador transistor NPN LM 317 matar o ripple ajust 3-12v

// fazer com que a variacao seja sempre mais alta do que 12V
// utilizar um diodo zenet para fazer esse corte
// somnte depois disso, ao utilizar um transistor eh possivel baixar a tensao para 3V com um botaozinho.

// colocar ao final um resistor que no pior caso seja 12v e 100mA, resistor Rc = 12v/ 0.1A = e deve sobreviver

// Ln317
# Circuito no FALSTAD

![circuit-20230625-1814](https://github.com/DeguShi/fonte_tensao/assets/136737102/46b71fd4-7749-4cef-997d-8118a78a2c39)

# Projeto do Esquemático da PCB no EAGLE

![EAGLE](https://github.com/DeguShi/fonte_tensao/assets/63174449/5fa2fe71-1880-49b5-b851-64adad062d8c)


![EAGLE - Fonte de Tensão](https://github.com/DeguShi/fonte_tensao/assets/63174449/f38924f6-60d4-4eec-bae7-0e1fc12d2f27)

# Componentes:

Os componentes do circuito são os seguintes:

1. Transformador: é o primeiro componente do circuito, localizado após a fonte de corrente alternada (tomada). Sua função é reduzir a tensão elétrica de 127V para o valor desejado pelo projeto, que varia entre 3V e 12V. O transformador escolhido é capaz de abaixar a tensão de 110V para 12V. É importante destacar que o transformador apenas altera o valor da diferença de potencial entre seus terminais, não convertendo a corrente alternada em corrente contínua.

2. Fusível: é um dispositivo de segurança que impede a passagem de correntes muito altas, protegendo os dispositivos do circuito contra picos de corrente indesejados.

3. Varistor: é outro dispositivo de segurança que, em conjunto com o fusível, protege o circuito contra sobretensão proveniente da rede elétrica.

4. Ponte de diodo: é utilizada para permitir que o circuito seja alimentado pela corrente em ambos os ciclos da corrente alternada.

5. Capacitor: tem a função de armazenar carga durante os ciclos da corrente alternada, liberando corrente quando a tensão interna é maior que a tensão proveniente da fonte. Ele se descarrega quando ocorre a inversão do ciclo. Para este projeto, foi escolhido um capacitor com um valor de capacitância de 458μF, visando um ripple de 10%. Como não existem capacitores com esse valor exato, foi selecionado um capacitor comercial próximo, com valor de 470μF.

6. Diodo Zener: atua como um regulador de tensão máxima. Ele só permite a passagem de corrente quando a tensão atinge o valor nominal do diodo, que neste caso é de 12V. Se a tensão for menor do que 12V, o diodo Zener não conduzirá corrente e não interferirá no circuito. No entanto, se a tensão for maior, ele permitirá a passagem da corrente, mantendo a tensão em 12V naquele ponto. Em resumo, o diodo Zener "trava" o valor da tensão em 12V, que é exatamente o valor máximo de tensão desejado na saída da fonte.

7. Resistores: são utilizados para complementar o circuito, limitando a corrente e garantindo que ela não ultrapasse os valores limite dos componentes.

8. Potenciômetro: trata-se de um resistor variável que permite o controle do valor da tensão resultante, ajustando-a entre 3V e 12V.

9. Transistor: é utilizado para controlar a passagem da corrente de forma ajustável, permitindo regular a intensidade da corrente no circuito.

| Componentes |	Info_extra | Valor |
|-------------|------------|-------|
|Transformador|     12 V   | 39,50 |
|Ponte de Diodos |	1N4007 |R$0,10 x 4 = R$0,40 |
|Capacitor	| 1000uF	| R$0,79 |
|Resistor	| 1kΩ	| R$0,05 |
|Resistor	| 820Ω	| R$0,05 |
|Resistor	| 4k7Ω	| R$0,05 |
|Led	| 5mm	| R$0,25 |
|Diodo Zener | 13V	| R$0,19 |
|Potenciômetro	| 10k	| R$1,79 |
|Transistor	| NPN	| R$0,29 |
|    | Valor total    | X reais | 

# responsaveis

Felipe de Castro Azambuja - 14675437

Gabriel de Andrade Abreu - 14571362

Guilherme Pascoale Godoy - 14576277

Isabela Beatriz Sousa Nunes Farias - 13823833


falstad copia e cola no importar por texto

falstad

$ 1 0.000005 13.097415321081861 49 5 43 5e-11
v 80 448 80 512 0 1 60 180 0 0 0.5
d 160 512 192 480 2 1N4004
d 192 544 224 512 2 1N4004
d 192 544 160 512 2 1N4004
d 224 512 192 480 2 1N4004
w 192 480 192 352 0
c 352 352 352 592 0 0.001 15.579227263288606 0.001
34 13v 1 1.7143528192810002e-7 0 2.283758940890054 13 2
z 576 592 576 464 2 13v
174 720 464 736 528 1 10000 0.005 Resistance
t 736 496 784 496 0 1 -2.7080288703180138 0.7147540195230562 100 default
r 816 512 816 592 0 120
r 720 528 720 592 0 4700
r 576 352 576 464 0 819.9999999999999
w 576 464 720 464 0
w 576 592 720 592 0
w 720 592 784 592 0
w 576 352 784 352 0
w 784 352 784 480 3
162 464 352 464 464 2 default-led 1 0 0 0.01
r 464 464 464 592 0 1000
w 352 352 464 352 3
w 464 352 576 352 0
w 352 592 464 592 0
w 464 592 576 592 0
w 192 352 352 352 0
g 352 592 352 656 0 0
w 192 592 336 592 0
w 336 592 352 592 0
403 624 640 752 704 0 7_64_0_4099_20_0.003125_-1_2_7_3
403 624 640 752 704 0 7_64_0_4099_20_0.003125_-1_2_7_3
w 784 512 816 512 3
w 784 592 816 592 0
169 80 448 144 448 0 4 0.1 -0.36093680993621635 0.7800316788508572 0.780031678850857 0.99
w 144 448 224 448 0
w 224 448 224 512 0
w 144 512 160 512 0
w 192 592 192 544 0
o 10 128 0 4099 20 0.2 0 2 10 3
o 7 4 0 4099 20 0.00625 1 2 7 3
o 24 64 0 4099 40 6.4 2 2 24 3
o 6 16 0 4099 40 1.6 3 2 6 3
o 30 16 0 4099 20 0.2 4 2 30 3
o 10 16 0 4099 20 0.2 5 2 10 3
o 9 16 6 4098 10 0.1 6 1
o 11 16 0 4099 5 0.0015625 7 2 11 3

