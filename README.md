Open source Kanban board.
[Official website](https://restya.com/board) and [demo](https://restya.com/board/demo).

## Simple `docker-compose.yml`

```
restyaboard:
  image: gdeflaux/restyaboard-ldap
  ports:
    - "80:80"
  links:
    - postgres
  volumes:
    - /volume/path/config:/etc/restyaboard
    - /volume/path/media:/var/nginx/html/media
postgres:
  image: postgres
  environment:
    - POSTGRES_USER=postgres
    - POSTGRES_PASSWORD=restyaboard
```

## Default users

```
Username: admin
Password: restya

Username: user
Password: restya
```
