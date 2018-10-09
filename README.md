#  Упражнения с данными: Вложенные массивы

## Введение

Массивы являются полезными объектами для хранения коллекций данных: списка чисел, строк или того, что у вас есть. Это довольно простые объекты, и их гибкость приводит к неограниченным возможностям их использования. Один общий шаблон проектирования, с которым мы будем иметь дело, - это *Вложенный массив*. Массив, элементами которого являются сами массивы. Другими словами, массив массивов.


## Release
### Release 0: Создание поля для игры “Крестики – нолики”

```javascript
generateTicTacToe
# => [["X", "O", "X"], ["O", "O", "X"], ["X", "X", "O"]]
generateTicTacToe
# => [["O", "O", "X"], ["X", "X", "O"], ["O", "O", "X"]]
```
*Рисунок 4*. Генерирование tic-tac-toe.

В упражнении на отработку  вложенных массивов мы написали методы, которые сумели вернули один конкретный вложенный массив. В этом выпуске мы снова напишем метод, который возвращает вложенный массив, но в этом случае мы хотим дополнительно добавить элемент случайности.

Мы собираемся написать метод `generateTicTacToe`, который возвращает вложенный массив, представляющий доску для игры в «Крестики – нолики». Доска должна быть заполнена X (крестиками) и O (ноликами). Мы можем решить, насколько реалистичной будет наша доска (например, четыре из одной буквы и пять других, только один победитель и т. Д.). Единственное правило состоит в том, что доска должна быть полностью заполнена знаками Х и О.


- Доска имеет три ряда.
- Каждая строка имеет три столбца.
- Доска только содержит X и O – и никаких других элементов.


### Release 1: Преобразование вложенного массива табличных данных 

```javascript
let tableData = [
  ["firstName", "lastName", "city", "state"],
  ["Elisabeth", "Gardenar", "Toledo", "OH"],
  ["Jamaal", "Du", "Sylvania", "OH"],
  ["Kathlyn", "Lavoie", "Maumee", "OH"]
]

convertTable(tableData)
# => [
#  { "firstName" => "Elisabeth", "lastName" => "Gardenar", "city" => "Toledo", "state" => "OH" },
#  { "firstName" => "Jamaal", "lastName" => "Du", "city" => "Sylvania", "state" => "OH" },
#  { "firstName" => "Kathlyn", "lastName" => "Lavoie", "city" => "Maumee", "state" => "OH" }
# ]
```
*Рисунок 5*. Преобразование данных таблицы в массив обьектов.

В этом выпуске мы преобразуем вложенный массив в массив обьектов. Другими словами, мы преобразуем массив, состоящий из массивов, в массив, состоящий из хешей. Давайте напишем метод `convertTable`, который берет вложенный массив, представляющий таблицу данных, и преобразует каждую строку данных в хэш, используя данные строки заголовка таблицы в виде ключей (см. Рис. 5).

## Выводы

В этой задаче мы научились работать с массивами. Прежде чем двигаться дальше, следует удостовериться, что мы ответили на любые вопросы, возникшие по ходу разбора этого задания.
