# getList
```php
getList(array $params = [])
```
Возвращает **массив строк** в соответствии с переданным параметром. Единственный параметр функции $params не является обязательным.

пример
```php
getList([
  'select' => ['id', 'name'], // массив полей
  'filter' => ['id' => $id], // массив параметров для фильтра
  'order' => ['name' => 'asc'],
  'group' => ['name'],
  'limit' => [$offset, $rowcount]
]);
```

## ключи $params
Ключи в массиве `$params` необязательны. Могут быть перечислены в любом порядке или отсутствовать вовсе.

### select
примеры
```php
'select' => [] // все поля модели, того же эффекта можно добиться не указывая этого параметра вообще
'select' => ['id', 'name', 'code']
```

### filter
примеры
```php
'filter' => ['name' => 'bitrix']
'filter' => ['name' => 'bitrix', 'sort' => 500]
```

### order
примеры
```php
'order' => ['name']
'order' => ['name' => 'asc']
'order' => ['name' => 'ASC']
'order' => ['name' => 'desc']
```
первые три примера эквивалентны

### group
примеры
```php
'group' => ['name']
'group' => ['name', 'sort']
```

### limit
примеры
```php
'limit' => [10] // первые 10 строк
'limit' => [10, 5] // пропускает 10 строк, возвращает следующие 5 строк
```
