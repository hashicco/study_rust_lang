# Study Rust Language

This repository is very very private.  
I'm studying Rust Language in docker container.

https://rust-lang-ja.github.io/the-rust-programming-language-ja/1.6/book/README.html

## required
- docker
- docker-compose

## How to start.

### prepare `.bash_profile` and `.env`

``` bash
touch .bash_profile
touch .env
```

### up docker container
``` bash
./docker-compose-dev up -d
```

### login to conrainer
``` bash
docker exec -it rust /bin/bash --login
```

### let's start study Rust.

``` bash
cargo new hogehoge --bin
cd hogehoge
```
