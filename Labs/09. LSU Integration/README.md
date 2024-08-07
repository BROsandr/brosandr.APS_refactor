# Лабораторная работа 9 "Интеграция блока загрузки и сохранения"

После реализации блока загрузки и сохранения, его необходимо интегрировать в процессорную систему. На _рис. 1_ представлена схема, иллюстрирующая интеграцию компонентов:

![../../.pic/Labs/lab_08_lsu/fig_01.drawio.svg](../../.pic/Labs/lab_08_lsu/fig_01.drawio.svg)

_Рисунок 1. Подключение LSU в процессорную систему._

## Задание

Интегрировать модуль `riscv_lsu` в модуль `riscv_unit`.

## Порядок выполнения работы

1. Интегрируйте модули `riscv_lsu` и `ext_mem` в модуль `riscv_unit`.
   1. Обратите внимание, что из модуля `riscv_unit` необходимо убрать логику сигнала `stall`, т.к. она была перемещена внутрь модуля `riscv_lsu`.
2. После интеграции модулей, проверьте процессорную систему с помощью [программы](../07.%20Datapath/#Задание) из ЛР№7.
   1. Обратите внимание на то, как теперь исполняются инструкции `sw`, `sh`, `sb`, `lw`, `lh`, `lb`, `lhu`, `lbu`.
