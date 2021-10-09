# VTB_more_tech_3_2021

# Запрос данных из системы с помощью файла
Для получения необходимых данных заказчик может сформировать запрос необходимых данных, зафиксировав требования с помощью следующих правил:

## Общая структура файла:
columns:
  col1
  col2
  ...
tables:
  tableA
  ...
join:
  body:
    source: tableA
    target: tableB
    source_on: tableA.col1
    target_on: tableB.col1  
  body:
  ...
filter:
  body:
    column: tableA.col2
    op: Eq
    value: 1
  body:
  ...
group_by:
  tableA.col1
  ...






columns:
  tableA.col1
  tableB.col2
  sum(tableA.col3 * 12)
  count(*)
tables:
  tableA
  tableB
join:
  body:
    source: tableA
    target: tableB
    source_on: tableA.col4
    target_on: tableB.col4    
filter:
  body:
    column: tableA.col5
    op: Eq
    value: 1488 
group_by:
  tableA.col1
  tableB.col2
