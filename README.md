# analog-signal-streaming

## Цель: 
Реализовать систему, которая будет получать аналоговый необработанный потоковый сигнал, отчищать его с помощью фитра Калмана, затем передавать сигнал в другой поток выполнения, который будет прогонять данные через нейронку и на выходе получать классифицированный результат.

## Стек:
C/C++, Conan, CMake, ZeroMQ, фильтр Калмана

## Полезные статьи
1) Теория по фильтру Калмена - https://habr.com/ru/articles/166693/
2) ZeroMQ на С++ - https://zeromq.org/get-started/?language=cpp&library=zmqpp#
