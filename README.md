# first-s2i-python-app

This is my first try using the source-2-image tool to get a skeleton django up 
and running

## Helpful references

* https://github.com/openshift/source-to-image
* https://hub.docker.com/r/centos/python-35-centos7/
* https://github.com/sclorg/s2i-python-container/tree/master/3.5

## Image Build Shortcuts

### To build image

```sh
s2i build ./helloworld centos/python-35-centos7 first-s2i-python-app-image
```

### To run the django app using runserver
```sh
docker run -p 8080:8080 first-s2i-python-app-image
```
and then you should be able to see "It Worked!" if you load http://127.0.0.1:8080
