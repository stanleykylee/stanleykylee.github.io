---
title:  "Docker-compose Optimization"
header:
  teaser: ""
categories: 
  - blog
tags:
  - docker
---

understanding how docker images are build
- layers
- size of image
- what get changed in those layers

updated docker file to use alpine instead of ubuntu
remove steps and compressed steps
used fromlatest.io for verification
changed the order of layers
reduced dependency of similar image and reuse created iamges instead

sped up time from 239s to 99s > 51s with alpine image built