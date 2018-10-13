### Docker run
```
docker run -p 5432:5432 -v /path/to/postgres/data:/var/lib/postgresql/data postgres:10

```
### Docker compose
```
version: '2'

services:
    postgres:
          restart: always
          image: postgres:10
          ports:
            - "5432:5432"
          environment:
            - POSTGRES_USER=postgres
            - POSTGRES_PASS=postgres
            - POSTGRES_DB=postgres
          volumes:
            - /path/to/postgres/data:/var/lib/postgresql/data
          networks:
            - code-network
networks:
    code-network:
        driver: bridge
```
