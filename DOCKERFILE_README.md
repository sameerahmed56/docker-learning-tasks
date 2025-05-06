# Docker File

- A Dockerfile is a text document that contains all the commands a user can call on the command line to assemble an image.
- Dockerfiles are a blueprint for building your Docker container images. 
- Each instruction in a Dockerfile creates a new layer in the image, and the final image is composed of all the layers stacked on top of each other.

## Best Practices
- Use multi-stage builds
- Create reusable stages
- Choose the right base image
- Rebuild your images often
- Exclude with .dockerignore
- Create ephemeral containers
- Don't install unnecessary packages
- Decouple applications
- Sort multi-line arguments
- Leverage build cache
- Pin base image versions
- Build and test your images in CI

## What To DO
- Use the COPY instruction to copy only the necessary files. Avoid executing instructions such as `COPY . .`
- Only install what you need. For example, use the `--no-install-recommends` option
- Group similar commands. For example: `RUN apt-get update && apt-get install -y curl`
- Remove the package manager cache: `rm -rf /var/lib/apt/lists/*`
- Use a specific image tag; avoid the `latest` tag
- Set non-root user and group
- Disallow acquiring new privileges
- Use only trusted and official base images
- Don’t store secrets or sensitive information in Dockerfile
- Don’t install SSH or similar services that may expose your containers
- Apply image lifecycle management updates, if required