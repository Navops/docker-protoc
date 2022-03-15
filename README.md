# docker-protoc

This repository builds a Docker images for generating code from [Protocol Buffer](https://developers.google.com/protocol-buffers) definitions.
At present, there is only one tag (`go-grpc`), which generates Go code using the Go and Go-gRPC plugins for `protoc` (protobuf compiler).

## Manual build/push
The image is built and pushed automatically via Github Actions, but here are instructions for a manual build/push.

### Build the image 
```
docker build . -t quay.io/navops/protoc:go-grpc -f Dockerfile.go-grpc
```

### Log in
If you haven't logged in to the private repository previously, do
```
docker login quay.io
```

### Push the image
```
docker push quay.io/navops/protoc:go-grpc
```
