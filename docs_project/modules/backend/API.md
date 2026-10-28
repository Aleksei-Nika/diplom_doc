
| Cущности |     Создание      |     Редактирование      |         Удаление         |     Просмотр     |
| :------: | :---------------: | :---------------------: | :----------------------: | :--------------: |
| Location | POST<br>/location | PATCH<br>/location/{id} | DELETE<br>/location/{id} | GET<br>/location |
|  Asset   |  POST<br>/asset   |  PATCH<br>/asset/{id}   |  DELETE<br>/asset/{id}   |  GET<br>/asset   |
| MoveLog  | POST<br>/movelog  | PATCH<br>/movelog/{id}  | DELETE<br>/movelog/{id}  | GET<br>/movelog  |

```python
# удаление
await session.execute(delete(data).where(data.id == x))

# получени и обновление
obj = await session.execute(select(data).where(data.id == x)).scalar_one()
obj.name = 'Новое имя'
```
