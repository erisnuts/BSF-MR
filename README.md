# BSF-MR

Инструкция по заполнению BSF-каркаса
1. Определить в Problem-Parameters.h константные параметры модели BSF.
2. Определить в Problem-Parameters.h константные параметры задачи (размерность,
число уравнений и т.п.).
3. Определить в Problem-Types.h типы:   
  * PT_bsf_data_T – тип данных (текущее приближение), которые будут
передаваться каждому рабочему в задании в начале очередной итерации;
  * PT_bsf_mapElem_T – тип элемента списка Map;
  * PT_bsf_reduceElem_T – тип элемента списка Reduce.
4. Определить переменные (Problem Variables) и структуры данных (Problem
Structures) в Problem_Data.h.
5. Добавить в Problem-Forwards.h предописания пользовательских функций (User
Function Forwards).
6. Реализовать в Problem-Implementation.cpp пользовательские функции (User
Functions).
7. Реализовать в Problem-Implementation.cpp функцию PI_bsf_SetInitApproximation,
задающую начальное приближение.
8. Реализовать в Problem-Implementation.cpp функцию PI_bsf_Init, считывающую
(генерирующую) исходные данные задачи.
9. Реализовать в Problem-Implementation.cpp функцию PI_bsf_AssignListSize,
задающую длину списка.
10. Реализовать в Problem-Implementation.cpp функцию PI_bsf_SetMapSubList,
формирующую подсписок map.
11. Реализовать в Problem-Implementation.cpp функцию PI_bsf_CopyData.
12. Реализовать в Problem-Implementation.cpp функцию PI_bsf_MapF, выполняющую
унарную операцию над элементом списка map и присваивающую результат
элементу списка reduce.
13. Реализовать в Problem-Implementation.cpp функцию PI_bsf_ReduceF, выполняющую
бинарную операцию над элементами списка reduce.
14. Реализовать в Problem-Implementation.cpp функцию PI_bsf_ProcessResults,
вычисляющую следующую итерацию и проверяющую условие завершения
итерационного процесса.
15. Реализовать в Problem-Implementation.cpp функцию PI_bsf_ParametersOutput,
осуществляющую вывод исходных параметров задачи (допускается пустая
реализация).
16. Реализовать в Problem-Implementation.cpp функцию PI_bsf_IterOutput,
осуществляющую вывод результатов каждой итерации (допускается пустая
реализация).
17. Реализовать в Problem-Implementation.cpp функцию PI_bsf_ProblemOutput,
осуществляющую вывод конечного результата.
