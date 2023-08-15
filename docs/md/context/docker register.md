```docker-compose
version: '3'

services:
  registry:
    image: registry
    ports:
      - 80:5000
    volumes:
      - ./data/registry:/var/lib/registry
```