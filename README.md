# do-curl


This is a Depend on Docker project which comes operational out of the box 
and is configured with reasonable defaults, which can be customized as needed.


The project contains the following scripts:
* `config.sh` - open the configuration file .env in an editor so the project can be customized
* `build.sh` - build the container image
* `test.sh` - run container unit tests
* `push.sh` - push the container image to a registry
* `pull.sh` - pull the container image from a registry
* `run.sh [cmd]` - run the container, passing an argument overrides the default command
* `status.sh` - show container status - running, exited, etc.
* `logs.sh` - tail container logs
* `exec.sh [cmd]` - open a shell or execute a specified command in the running container

## Usage

Within project ( git clone https://github.com/iankoulski/do-curl.git ):
```
./run.sh
./exec.sh curl http://icanhazip.com
./stop.sh
```

On a docker host:

```
docker run -it --rm  iankoulski/do-curl curl http://icanhazip.com
```

In Kubernetes:

```
kubectl exec -it <pod-name> -- bash -c "curl http://icanhazip.com"
```


