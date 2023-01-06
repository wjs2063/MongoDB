fast api docs :  https://fastapi.tiangolo.com/
https://www.mongodb.com/developer/languages/python/python-quickstart-fastapi/



```
pip install fastapi

pip install "uvicorn[standard]"


```

create main.py

```
from typing import Union

from fastapi import FastAPI

app = FastAPI()


@app.get("/")
def read_root():
    return {"Hello": "World"}


@app.get("/items/{item_id}")
def read_item(item_id: int, q: Union[str, None] = None):
    return {"item_id": item_id, "q": q}

```

save


server start!!
```
uvicorn main:app --reload
```

접속 : http://127.0.0.1:8000/docs



```
from typing import Union

from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()


class Item(BaseModel):
    name: str
    price: float
    is_offer: Union[bool, None] = None


@app.get("/")
def read_root():
    return {"Hello": "World"}


@app.get("/items/{item_id}")
def read_item(item_id: int, q: Union[str, None] = None):
    return {"item_id": item_id, "q": q}


@app.put("/items/{item_id}")
def update_item(item_id: int, item: Item):
    return {"item_name": item.name, "item_id": item_id}

```

링크:   http://127.0.0.1:8000/redoc.
