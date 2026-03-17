## Docker Compose File

```yaml
services:
  web:
    build: .
    ports:
      - "5000:5000"
    depends_on:
      - db
      - redis

  db:
    image: postgres
    restart: always
    environment:
      POSTGRES_DB: testdb
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
    volumes:
      - pg-data:/var/lib/postgresql/data
    healthcheck:
      test: ["CMD-SHELL", "pg_isready -U user"]
      interval: 10s
      timeout: 5s
      retries: 3
      start_period: 30s

  redis:
    image: redis

volumes:
  pg-data:
```

---

## Dockerfile

```dockerfile
FROM python:3.14-slim

WORKDIR day34-proj

COPY . .

RUN pip install -r requirements.txt

CMD ["python", "app.py"]

EXPOSE 5000
```
