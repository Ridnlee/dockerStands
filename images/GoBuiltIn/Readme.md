### Docker run
```
docker run -p image_name
```
### Docker compose
```
version: '3'

services:
  go:
    build: ./
    networks:
      - code-network
networks:
  code-network:
    driver: bridge

```
