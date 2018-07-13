---
title: Docker
layout: notes
---

# Destroy all containers
```
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```
