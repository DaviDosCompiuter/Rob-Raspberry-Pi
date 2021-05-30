# Robo-Raspberry-Pi
Esse Github objetiva aplicar os conhecimentos da disciplina de sistemas embarcados do Instituto Federal de Campina Grande para obtenção de nota

A documentação para a reprodução do projeto está em "doc/Artigo.pdf"

Esse Projeto tem como objetivo desenvolver um protótipo em escala reduzida de um robô controlado remotamente através de uma comunicação Wi-Fi pelo usuário, através de um computador, que tem por finalidade atuar em áreas ou situações de desastre onde a intervenção humana é perigosa ou impraticável.


O esquemático da montagem abaixo ilustra todos os componentes utilizados na montagem:
```
*1 Raspberry Pi 3 Model B
*1 Notebook
*1 Ponte H L298N
*2 Motores DC 3-6V
*1 Pack de pilhas AAA
*1 PowerBank
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Hardware/Esquematico_de_montagem.png)

```
A simulação gerada a partir do proteus 8.9 está em "Simulador/Davi_Projeto_Proteus.pdsprj" junto com o codigo "Simulador/Codigo.txt" ilustrada abaixo
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Hardware/Esquematico_Proteus.png)

O projeto consiste em um carrinho que se comunica por Wi-Fi com um computador através de um acesso remoto "SSH". Para o movimento do robô é necessário controlar as entras do driver de motor(L298N) através de 4 entradas Enable. Isso permite que o robô realize 4 operações:
```
Andar para frente: Colocando nível alto no EN1 e EN3 e nível baixo no EN2 e EN4
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/doc/R1.png)

```
Andar para trás: Colocando nível alto no EN2 e EN4 e nível baixo no EN1 e EN3
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/doc/R2.png)

```
Andar para direita: Colocando nível alto no EN1 e nível baixo no EN2, EN3 e EN4
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/doc/R3.png)
```
Andar para esquerda: Colocando nível alto no EN3 e nível baixo no EN1, EN2 e EN4
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/doc/R4.png)

O codigo do projeto está em "Software/Carrinho.py", onde está dividido em 3 partes:

```
Setup: Onde estão importadas as bibliotecas necessarias para a realização do projeto,
os GPIOS de controle do driver de motor(3,5,7 e 8 configurados como saída e inializados
em nível baixo para garantir que o robô não se movimente) e por fim uma mensagem de 
instrução para o usuário
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Software/C1.png)


```
Função: Onde estão apresentadas as funções frente, tras, direita, esquerda e pare antes mencionadas 
neste documento, com exceção da função pare que simplesmente para os motores
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Software/C2.png)



```
Repetição: Onde constantemente espera o comando de entrada do usuário para movimentação
do robô
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Software/C3.png)

```
A montagem final está ilustrada na imagem a seguir.
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Hardware/Montagem.jpg)

```
Um video demonstando a utilização do projeto é apresentado a seguir.
```
https://drive.google.com/file/d/1SQElVlmRWGI77ao3GvxEDGE3MhttOQvP/view?usp=sharing
