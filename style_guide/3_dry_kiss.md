# Работа с базами данных

## Общие правила
- Использовать подготовленные запросы для защиты от SQL-инъекций
- Закрывать соединения после работы
- Обрабатывать ошибки и исключения

## Пример на Python (sqlite3)
```python
import sqlite3

conn = sqlite3.connect('example.db')
try:
    cursor = conn.cursor()
    cursor.execute("SELECT * FROM users WHERE id=?", (user_id,))
    result = cursor.fetchall()
finally:
    conn.close()

