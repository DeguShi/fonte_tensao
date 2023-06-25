# fonte_tensao
Projeto de Eletrônica:

![image](https://github.com/DeguShi/fonte_tensao/assets/128547705/df8d362b-5213-41a0-98ea-7ec15fcac8c6)

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
