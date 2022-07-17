# busylight-docker
Dockerfile to build a [`busylight`](https://github.com/JnyJny/busylight) container. 

Make sure to add the `--device=/dev/bus` flag to your `docker run` command to allow access to USB devices.

## Buildng the container image

1. Clone this repository.
1. Inside the directory for this repository, run:
    ```shell
    docker build -t busylight-docker .
    ```

## Running the container

1. Run the following command:
    ```shell
    docker run -d --device=/dev/bus -p 8080:8080 busylight-docker:latest
    ```

_Explanation:_ adding the `--device=/dev/bus` flag allows the container to access USB devices (located under `/dev/bus/`)
