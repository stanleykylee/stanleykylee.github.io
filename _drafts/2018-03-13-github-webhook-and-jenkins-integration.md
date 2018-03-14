---
header:
  teaser: ""
categories: 
  - blog
tags:
  - jenkins
  - github
---

integration requires installation of github plugin
api key to connect
use of multibranch job to start
connect to github using account and list of all repos
with repo select, need a simple Jenkinsfile

```groovy
pipeline {
    agent any
    stages {
        stage ('Load SCM') {
            checkout scm
        }
    }
}
```