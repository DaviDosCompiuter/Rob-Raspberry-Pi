# Robo-Raspberry-Pi
Projeto para avaliação da disciplina de sistemas embarcados

O esquematico abaixo representa todos os componentes utilizados na montagem:
```
*1 Raspberry Pi 3 Model B
*1 Notebook
*1 Ponte H L298N
*2 Motores DC 3-6V
*1 Pack de pilhas AAA
*1 PowerBank
```

![img](https://github.com/DaviDosCompiuter/Robo-Raspberry-Pi/blob/main/Esquematico.png)

O projeto consiste em um carrinho que se comunica por Wi-Fi com um computador através de um acesso remoto "SSH". Para o movimento do robô é necessário controlar as entras do driver de motor(L298N) através de 4 entradas Enable. Isso permite que o robô realize 4 operações:
```
Andar para frente
```
