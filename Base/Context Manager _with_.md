#dev #python
# Context Manager "with"

### abstract
Контекстный менеджер - объект, который определяет логику входа и выхода из контекста выполнения кода.

Используеться для управления ресурсами, такими как файлы, сетевые соединения, базы данных

Гарантирует что ресурсы будут правильно и автоматически освобождены после завершения операций.

### syntax

Контекстные менеджеры используються с помощью ключевого слова `with` и реализуют два метода: `__enter__()` и `__exit__()`

Метод `__enter__()` при входе в контекст
Метод `__exit__()` при выходе из контекста

Это обеспечивает автоматическое управление ресурсами и обработку исключений.

С присваиванием объекта `context_manager.__text__` 
в переменную <code>variable</code>
```python
with <context_manager> as <variable>:
	construction_list
```

Без присваивания объекта переменной 
```python
with <context_manager>:
	construction_list
```

Создание объекта который может использоваться контекстным менеджером
```python
class Example:
	def __enter__(self):
		...

	def __exit__(self, exc_type, exc_value, traceback):
		...
```

### specific example

1. Работа с файлами
```python
with open('file.txt', 'w') as file:
	file.write('Hello, World!')
```

2. Соединение с базой данных
```python
import sqlite3

with slqlite3.connect('database.db') as database:
	cursor = database.cursor()
	cursor.execute('SELECT * FROM table')
	data = cursor.fetchall()
```

3. Загрузка ресурсов из сети
```python
import requests

with requests.Session() as session:
	response = session.get('https://example.com')
	...
```

4. Использование сокетов
```python
import socket

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as sock:
	sock.connect(('example.com', 80))
	sock.send(b'GET / HTTP/1.1\r\n\r\n')
	response = sock.recv(4096)
```

5. Временное изменение рабочего каталога
```python
import os

with os.chdir('directory'):
	print(os.getcwd())

print(os.getcwd())
```

6. Замер времени выполнения кода
```python
import time

class Timer:
	def __enter__(self):
		self.start_time = time.time()
		return self

	def __exit__(self, exc_type, exc_value, traceback):
		self.end_time = time.time()
		elapsed_time = self.end_time - self.start_time
		print(f'Code runtime {elapsed_time} sec')

with Timer():
	time.sleep(5)
```

7. Тот же самый пример с замером времени, только без создания класса Timer
```python
from contextlib import contextmanager
import time

@contextmanager
def time_it():
    start_time = time.time()
    try:
        yield
    finally:
        end_time = time.time()
        elapsed_time = end_time - start_time
        print(f'Code runtime {elapsed_time} sec')

with time_it():
	time.sleep(5)
```

### comparison

Использование контекстного менеджера:
- делает код более читаемым
- обеспечивает автоматическое управление ресурсами и гарантированное освобождение после завершения операций
- упрощает обработку исключений

### zero links
- [[00 Python]]

## references
- [Контекстный менеджер python. Менеджеры контекста python. Оператор with](https://www.youtube.com/watch?v=ycVlsU_c4Mg)
- [Python Context Managers and the "with" Statement (__enter__ & __exit__)](https://www.youtube.com/watch?v=iba-I4CrmyA)
