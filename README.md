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

//fazer com que a variacao seja sempre mais alta do que 12V
//utilizar um diodo zenet para fazer esse corte
// somnte depois disso, ao utilizar um transistor eh possivel baixar a tensao para 3V com um botaozinho.

// colocar ao final um resistor que no pior caso seja 12v e 100mA, resistor Rc = 12v/ 0.1A = e deve sobreviver


