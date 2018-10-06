### Management page:
```
http://localhost:15672/
```

### Docker run
```
docker run -p 15672:15672 -p 5672:5672 -p 5671:5671 -p 4369:4369 -p 15671:15671 image_name 
```
### Docker compose
```
version: '3'

services:
  rmq:
    build: ./
    ports:
      - "5672:5672"
      - "15672:15672"
      - "5671:5671"
      - "4369:4369"
      - "15671:15671"
    networks:
      - code-network
networks:
  code-network:
    driver: bridge

```
