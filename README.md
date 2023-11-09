# analog-signal-streaming

## Цель: 
Реализовать систему, которая будет получать аналоговый необработанный потоковый сигнал, отчищать его с помощью фитра Калмана, затем передавать сигнал в другой поток выполнения, который будет прогонять данные через нейронку и на выходе получать классифицированный результат.

## Стек:
C/C++, Conan, CMake, ZeroMQ, фильтр Калмана

## Полезные статьи
1) Теория по фильтру Калмена - https://habr.com/ru/articles/166693/
2) ZeroMQ на С++ - https://zeromq.org/get-started/?language=cpp&library=zmqpp#

## Как пользоваться Conan
    https://docs.conan.io/2/tutorial/consuming_packages/build_simple_cmake_project.html#
 
## Пример простой цепочки команд для запуска
    1) conan install conanfile.txt --build=missing
    2) cd build
    3) cmake .. -G "Unix Makefiles" -DCMAKE_TOOLCHAIN_FILE=./Release/generators/conan_toolchain.cmake -DCMAKE_POLICY_DEFAULT_CMP0091=NEW -DCMAKE_BUILD_TYPE=Release
    4) cmake --build .
    5) . bin/<project_name>

## Как ставить библиотеки без конона
Находим библиотеку на гитхабе. Идем по инструкции, которая должна показать как собрать и установить библиотеку.
После этого должна начать работать система поиска в cmake
