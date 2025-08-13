*Dockerfile*

```
FROM python:3.10-slim

WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 5000

CMD ["python", "main.py"]
```

---

*requirements.txt*

```
flask==2.3.2
requests==2.31.0
```

---

*main.py*

```python
from flask import Flask

app = Flask(_name_)

@app.route('/')
def home():
    return "Bienvenue sur Aizen!"

if _name_ == '_main_':
    app.run(host='0.0.0.0', port=5000)
``
