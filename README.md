# gitlab-dev

## Run
```sh
docker compose up
```

## Get "root" password
```sh
sudo docker exec -it gitlab grep 'Password:' /etc/gitlab/initial_root_password
```


## Open
http://localhost/


## STore Git Login

```sh
git config --global credential.helper store   # Caches in plaintext (~/.git-credentials)
```

## Cache Git Login

```sh
git config --global credential.helper cache   # Caches in memory (default 15 minutes)
```

```sh
git config --global credential.helper 'cache --timeout=86400'
```

## Test Login

```sh
git ls-remote http://git.home/root/test.git/
```