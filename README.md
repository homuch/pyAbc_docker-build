# abc_py Docker Build

It's a docker file for [abc_py](https://github.com/krzhu/abc_py). The image use python 3.12.3 and the package is installed in `/abc_py-venv`. The built image is available at https://hub.docker.com/repository/docker/chomu/abc_py.

## Build

```bash
  # in the directory of the Dockerfile
  source download_source_mac.sh
  docker build .
```

## Push
  
  ```bash
    # in the directory of the Dockerfile
    docker tag <image_id> chomu/abc_py:<platform> # amd64, arm64, ...
    docker push chomu/abc_py:latest
  ```

## Pull
  
  ```bash 
    # in any directory
    docker pull chomu/abc_py:latest --platform <platform> # linux/amd64, linux/arm64, linux/arm/v8 ...
  ```