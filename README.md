##  Вложенные массивы - Крестики-нолики и снова Таблица

Массивы являются полезными объектами для хранения коллекций данных: списка чисел, строк и тд. Это довольно простые объекты, и их гибкость приводит к неограниченным возможностям их использования. В этом задании рассматривается тема *Вложенные массивы*. Массивы, элементами которых являются массивы. Другими словами, массивы массивов.

### Release 0. Создание поля для игры “Крестики – нолики”

```javascript
generateTicTacToe()
//  => [["X", "O", "X"], ["O", "O", "X"], ["X", "X", "O"]]
generateTicTacToe()
//  => [["O", "O", "X"], ["X", "X", "O"], ["O", "O", "X"]]
```
*Рисунок 1*. Генерирование tic-tac-toe.

Тебе нужно написать метод `generateTicTacToe`, который возвращает вложенный массив, представляющий доску для игры в «Крестики – Нолики». Доска должна быть заполнена X (крестиками) и 0 (ноликами). Ты можешь решить, насколько реалистичной будет доска (например, четыре X буквы и пять 0 (то есть ноликов не может быть на 2 больше чем крестиков), только один победитель и т.д.). Единственное правило состоит в том, что доска должна быть полностью заполнена знаками Х и О.

- Доска имеет три ряда.
- Каждая строка имеет три столбца.
- Доска содержит только X и O – и никаких других элементов.


### Release 1. Преобразование вложенного массива табличных данных 

```javascript
let tableData = [
  ["firstName", "lastName", "city", "state"],
  ["Elisabeth", "Gardenar", "Toledo", "OH"],
  ["Jamaal", "Du", "Sylvania", "OH"],
  ["Kathlyn", "Lavoie", "Maumee", "OH"]
]

convertTable(tableData)
=> [
 { "firstName" : "Elisabeth", "lastName" : "Gardenar", "city" : "Toledo", "state" : "OH" },
 { "firstName" : "Jamaal", "lastName" : "Du", "city" : "Sylvania", "state" : "OH" },
 { "firstName" : "Kathlyn", "lastName" : "Lavoie", "city" : "Maumee", "state" : "OH" }
]
```
*Рисунок 2*. Преобразование данных таблицы в массив обьектов.

В этом релизе ты преобразуешь вложенный массив в массив обьектов. Другими словами, ты преобразуешь массив, состоящий из массивов, в массив, состоящий из объектов. Давай напишем метод `convertTable` (см. Рисунок 2).

## Выводы

В этой задаче ты научился(ась) работать с массивами. Прежде чем двигаться дальше, следует удостовериться, что ты ответил(а) на все вопросы, возникшие по ходу разбора этого задания.
