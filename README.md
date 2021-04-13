# Docker

### Tools as docker containers
### Jfrog Artifactory
```
----- With Volume -----

mkdir -p artifactory/var
chmod 755 artifactory/var
sudo chown 1030:1030 -R artifactory/var
docker run --name artifactory -d -p 8081:8081 -p 8082:8082 -v $(pwd)/artifactory/var:/var/opt/jfrog/artifactory releases-docker.jfrog.io/jfrog/artifactory-oss:7.5.5

----- Without volume -----

docker run --name artifactory -d -p 8081:8081 -p 8082:8082 releases-docker.jfrog.io/jfrog/artifactory-oss:7.5.5
```

### Jenkins
```
----- With Volume -----

docker run --name jenkins -d -p 8080:8080 -p 50000:50000 -v jenkins-volume:/var/jenkins_home jenkins/jenkins:2.263.3

----- Without Volume -----
docker run --name jenkins -d -p 8080:8080 -p 50000:500000 jenkins/jenkins:2.263.3

```

### Mysql 5.6
```
----- Without Volume -----
docker run --name mysql -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=test mysql:5.6
```

### Reference
Udemy-docker-mastery by bretfisher, examples are here: https://github.com/vigneshsweekaran/udemy-docker-mastery

Security best practise: https://github.com/BretFisher/ama/issues/17
