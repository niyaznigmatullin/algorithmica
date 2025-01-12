---
title: Дек
weight: 7
draft: true
---

`dequeue` - структура, позволяющая работать и с началом и концом
одновременно, то есть вставка и удаление с двух сторон

``` C++
dequeue<T> name; // дек типа T с названием name
name.front(), name.back(); // ссылка на первый и последний элемент соответственно
name.pop_front(), name.pop_back(); // удаление первого и последнего элемента
name.push_front(x), name.push_back(x); // вставка x в начало/конец
```

Дек - это структура данных, которая тоже хранит упорядоченные элементы с
такими операциями за $O(1)$:

  - `push_back(x)` - положить элемент в конец дека
  - `push_front(x)` - положить элемент в начало дека
  - `pop_back()` - вынуть и вернуть элемент из конца дека
  - `pop_front()` - вынуть и вернуть элемент из начала дека

То есть очередь и стек можно реализовать с помощью дека. Чаще всего
удобно вместо очереди использовать именно дек.

Один из способ реализации дека --- с помощью закольцованного буфера.
