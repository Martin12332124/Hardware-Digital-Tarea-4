# Tarea 4 - ISF-215 Hardware Digital
Módulo: ALU simple de 2 bits

Este repositorio contiene el circuito que diseñé para la Tarea 4. Elegí armar una pequeña ALU (Unidad Aritmético Lógica) de 2 bits, que básicamente es el "cerebro" matemático de un procesador. En lugar de usar microcontroladores, diseñé toda la lógica desde cero utilizando exclusivamente compuertas lógicas discretas (chips de la familia 74HC).

¿Que es lo que hace?
El circuito recibe dos bits de datos a través de un interruptor (entradas A y B). La parte interesante está en los otros dos interruptores de control (S1 y S0); dependiendo de cómo los combines, la ALU cambia su comportamiento y decide qué operación aplicarle a los datos:
 Puede multiplicarlos lógicamente (AND).
 Puede sumarlos lógicamente (OR).
 Puede aplicar una compuerta exclusiva (XOR).
 O puede hacer una suma binaria matemática pura.

¿Cómo leer los resultados?
Para que sea fácil de visualizar en la simulación, implementé dos luces LED que te muestran exactamente qué está pasando:
El LED Rojo (Resultado): Es la salida principal. Te muestra el resultado de la operación que los selectores le ordenaron hacer a la ALU.
El LED Amarillo (Acarreo / Carry): Este tiene un trabajo especial. Solo se activa cuando estás en el modo de "Suma" y sumas 1 + 1. Como en binario eso da "10", el LED rojo se apaga (0) y este LED amarillo se prende (1) para avisar que lleva una unidad extra hacia el siguiente bit.

Intente reducir las ecuaciones booleanas usando mapas de Karnaugh para optimizar la cantidad de compuertas que usaba el simulador. Puede entrar, mover los interruptores y ver cómo responde en tiempo real en el tinkercad:

[Tinkercak](https://www.tinkercad.com/things/jCmXH3GKCOe-alu-2bits)
