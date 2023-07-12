# Fonte de Tensão Regulável 3v - 12v (100mA)

# Introdução
O seguinte projeto, desenvolvido para a disciplina de Eletrônica para computação, tem como objetivo aplicar os conhecimentos adquiridos em aula para projetarmos uma fonte de tensão ajustável entre 3V e 12V e com corrente de 100mA.

# Circuito no FALSTAD

![circuit-20230712-1205](https://github.com/DeguShi/fonte_tensao/assets/63174449/8fa7c1db-0263-4554-b645-c20487837946)


Link: https://www.falstad.com/circuit/circuitjs.html

# Projeto do Esquemático da PCB no EAGLE

 ![EsquematicoEagle](https://github.com/DeguShi/fonte_tensao/assets/63174449/3901130e-a663-4ef7-a4eb-f32c02dfdd5a)


  ![Eagle](https://github.com/DeguShi/fonte_tensao/assets/63174449/ab4cbca0-6561-4ba7-b037-2ef0b0091151)

# Componentes:

Os componentes do circuito são os seguintes:

1. Transformador: é o primeiro componente do circuito, localizado após a fonte de corrente alternada (tomada). Sua função é reduzir a tensão elétrica de 127V para o valor desejado pelo projeto, que varia entre 3V e 12V. O transformador escolhido é capaz de abaixar a tensão de 110V para 12V. É importante destacar que o transformador apenas altera o valor da diferença de potencial entre seus terminais, não convertendo a corrente alternada em corrente contínua.

2. Diodo retificador: é utilizada para permitir que o circuito seja alimentado pela corrente em ambos os ciclos da corrente alternada.

3. Capacitor: tem a função de armazenar carga durante os ciclos da corrente alternada, liberando corrente quando a tensão interna é maior que a tensão proveniente da fonte. Ele se descarrega quando ocorre a inversão do ciclo. Para este projeto, foi escolhido um capacitor com um valor de capacitância de 458μF, visando um ripple de 10%. Como não existem capacitores com esse valor exato, foi selecionado um capacitor comercial próximo, com valor de 470μF.

4. Diodo Zener: atua como um regulador de tensão máxima. Ele só permite a passagem de corrente quando a tensão atinge o valor nominal do diodo, que neste caso é de 12V. Se a tensão for menor do que 12V, o diodo Zener não conduzirá corrente e não interferirá no circuito. No entanto, se a tensão for maior, ele permitirá a passagem da corrente, mantendo a tensão em 12V naquele ponto. Em resumo, o diodo Zener "trava" o valor da tensão em 12V, que é exatamente o valor máximo de tensão desejado na saída da fonte.

5. Resistores: são utilizados para complementar o circuito, limitando a corrente e garantindo que ela não ultrapasse os valores limite dos componentes.

6. Potenciômetro: trata-se de um resistor variável que permite o controle do valor da tensão resultante, ajustando-a entre 3V e 12V.

7. Transistor: é utilizado para controlar a passagem da corrente de forma ajustável, permitindo regular a intensidade da corrente no circuito.

| Componentes |	Info_extra | Valor |
|-------------|------------|-------|
|Transformador|     12 V   | 39,50 |
|Diodo Retificador |	1N4007 |R$0,10 x 2 = R$0,20 |
|Capacitor	| 1000uF	| R$0,79 |
|Resistor	| 1kΩ	| R$0,05 |
|Resistor	| 820Ω	| R$0,05 |
|Resistor	| 3k3Ω	| R$0,05 |
|Led	| 5mm	| R$0,25 |
|Diodo Zener | 13V	| R$0,19 |
|Potenciômetro	| 10k	| R$1,79 |
|Transistor	| NPN	| R$0,29 |
|    | Valor total    | 43.16 reais | 

# Cálculos 

Capacitor:

C = i * (2*f*Vpico*Ripple)^-1

Ripple desejado é de aproximadamente 6.0%
Valor de i obtido no falstad: 120.3mA
Valor de Vpeak obtido também no falstad 16.9V
Frequêcia de 60Hz

C= (120.3*10^-3)*(120*16.9*0.06)^-1 
C é aproximadamente de 1016uF, porém para fins comerciais adotamos 1mF;

Resistores:

Para o LED atribuimos uma resistência de 1000 ohms para que ficasse bem brilhoso, porém poderia ser um pouco maior para que aquecesse menos.

Para o resistor que acompanha o Zener, seria necessária uma corrente de aproximadamente 4.5mA e a tensão medida no falstad era de 3.9V
isso nos deu uma resistência de 866 ohms, regulada para 820 em valores comerciais, obtendo em média 4.5mA de corrente.

Tensão Final:

O zener limita a tensão para 13V e, ao passar pelo transistor (no falstad ele ocorre depois de passar pelo potenciômetro) perde 0.7V, resultando em 12.3 (após testar o trabalho físico alteramos o falstad e agora ele passa 12.2).

Quando a tensão a ser obtida é 3V:

Isso acontece quando o potenciômetro está maximizado em 10kohms.

12.2 - Vpot = 3, o que daria 9.2V, porém no falstad obtivemos 9.771V

Para o valor de 9.771V o valor de tensão obtida na saída foi de aproximadamente  2.8V quando o potenciômetro está em 10kohm. 
É fundamental, nesse caso, a existencia de um resistor paralelo com a saida (carga) e consequentemente em série com o potenciômetro para evitar que toda a tensão seja consumida por esse.

o valor dessa resistência era de 4.7k incialmente, porém após a testagem do circuito na protoboard verificou-se a necessidade de diminuí-la, sendo um resistor de 3.3k o escolhido para tal.

Quando a tensão a ser obtida for 12V:

Isso acontece quando o potenciômetro está em 50ohms, seu valor mínimo.
Nesse caso, em teoria a tensão completa que ainda está no potenciômetro e no resistor em série a ele é liberada, sendo uma saída de 12.3V (após a mudança de resistor a saída passou a ser 12.2V).

# Integrantes:

Felipe de Castro Azambuja - 14675437

Gabriel de Andrade Abreu - 14571362

Guilherme Pascoale Godoy - 14576277

Isabela Beatriz Sousa Nunes Farias - 13823833
