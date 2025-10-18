# Логические операторы и условия

## Примеры
- Использовать guard clauses для упрощения вложенных if:
```python
if not user.is_authenticated:
    return redirect('/login')

