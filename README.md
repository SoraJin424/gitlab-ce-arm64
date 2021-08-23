# GitLab Docker images for arm64

The original introduction could be found [here](https://hub.docker.com/r/gitlab/gitlab-ce/).

The following is an example of how to use the image.
```
docker run --detach \
  --hostname gitlab.example.com \
  --publish 443:443 --publish 80:80 --publish 22:22 \
  --name gitlab \
  --restart always \
  --volume $GITLAB_HOME/config:/etc/gitlab:Z \
  --volume $GITLAB_HOME/logs:/var/log/gitlab:Z \
  --volume $GITLAB_HOME/data:/var/opt/gitlab:Z \
  sorajin/gitlab-ce-arm64:latest
```


