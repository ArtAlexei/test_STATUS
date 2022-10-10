# Тестовое задание

Согласно ТЗ нам нужен "прямой доступ к элементам без поиска их в массиве."
Для этого я решил:
- хранить данные в словаре у которого доступ по id будет иметь константную сложность - O(1)
- чтобы уменьшить сложность метода getChildren() я решил денормализовать данные, и хранить так же информацию о потомках элемента в дереве.

### Пример хранения данных
```
storage = {
    1: {"parent": "root", "children": [2, 3]},
    2: {"parent": 1, "type": "test", "children": [4, 5, 6]},
    3: {"parent": 1, "type": "test", "children": []},
    4: {"parent": 2, "type": "test", "children": [7, 8]},
    5: {"parent": 2, "type": "test", "children": []},
    6: {"parent": 2, "type": "test", "children": []},
    7: {"parent": 4, "type": None, "children": []},
    8: {"parent": 4, "type": None, "children": []},
}
```




