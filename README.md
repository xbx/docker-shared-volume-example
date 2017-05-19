# Simple example of docker shared volumes

```
docker-compose up
```

Equivalent to:

```
docker run -v ${PWD}/shared/:/var/log/shared/ -t -d ubuntu sh -c "while true; do date | tee -a /var/log/shared/app.log; sleep 1; done"
docker run -v ${PWD}/shared/:/var/log/shared/ -t ubuntu sh -c "tail -F /var/log/shared/app.log"
```
