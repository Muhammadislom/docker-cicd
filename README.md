# cicd

```
 mkdir -p /data/docker/gitlab/var/opt/gitlab
```
```
 mkdir -p /data/docker/gitlab/var/log/gitlab
```
```
 mkdir -p /data/docker/gitlab/etc/gitlab-runner
```
```
 mkdir -p /data/docker/gitlab/var/run/docker.sock
```
```
 docker-compose up -d --force-recreate && docker-compose ps
```

#Узнать пароль для учетки root из web-панели GitLab:

```
 docker exec -it gitlab_gitlab_1 grep 'Password:' /etc/gitlab/initial_root_password
```

#Установить свой пороль для root. Команда из контейнера
```
 sudo gitlab-rake "gitlab:password:reset[root]"
```
