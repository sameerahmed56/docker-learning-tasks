# TASK-1

## Build and Run
```
docker build -t <image-tag-name> .
docker run -p 3000:3000 <image-tag-name>
```

## Tag and Push
```
docker tag imagename:tag username/imagename:tag
docker push username/imagename:tag
```

## Pull and Run Image
```
docker run username/imagename:tag
```

## Multi Arch Build

```
docker buildx build \
  --platform linux/amd64,linux/arm64 \
  -t username/imagename:tag  \
  --push .
```