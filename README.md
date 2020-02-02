# Docker Registry Demo

Run the [Docker Registry](https://docs.docker.com/registry/) and an accompanying [GUI made by Quiq](https://github.com/Quiq/docker-registry-ui) with a simple `docker-compose.yml` file.

## Setup

```bash
git clone https://github.com/mewil/registry-docker-demo
cd registry-docker-demo
docker-compose up -d
```

Open http://localhost:8000/ in your browser to see the registry GUI.

To push an [alpine Docker image](https://hub.docker.com/_/alpine/) to your local registry run the following commands:

```bash
docker pull alpine:latest
docker tag alpine:latest localhost:5000/alpine:latest
docker push localhost:5000/alpine
```

To view the logs run `docker-compose logs -f` and to stop and remove the containers, run `docker-compose down`.
