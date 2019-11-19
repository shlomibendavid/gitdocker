# gitdocker

The gitdocker image is used to work (i.e clone,push,pull etc) with git repositories.
It based on the ubuntu latest distro and includes a git package.

## installation
You can either pull the gitdocker image or build it yourself

To pull the gitdocker image
```
docker pull shlomibendavid/gitdocker
```

To build it
```
docker image build -t shlomibendavid/gitdocker .
```
**NOTE:** i'm assuming that you are running the above command from the current directory (where the Dockerfile is located)

## usage
1. Create a docker container
```
docker container run --detach -it --name gitdocker --restart always shlomibendavid/gitdocker
```

2. Clone a git repository into the container
```
docker container exec -it gitdocker git clone https://<github repository>
```
**NOTE:** make sure to replace the <github repository> with your relevant one
