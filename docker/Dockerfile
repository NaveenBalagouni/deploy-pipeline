# Use the Bitnami Kaniko executor image
FROM bitnami/kaniko:latest

# Set the environment variables for Docker registry and image
ENV DOCKER_REGISTRY=quay.io
ENV DOCKER_IMAGE=opsmxpublic/baseline-issuegen
ENV IMAGE_TAG=v11

# Kaniko build context and Dockerfile path (can be mounted)
ARG CONTEXT_PATH=/mnt/git-repo
ARG DOCKERFILE_PATH=docker/Dockerfile

# Use a volume to mount the context and Dockerfile
VOLUME ["/mnt/git-repo"]

# Run Kaniko executor with the provided build context and Dockerfile
CMD ["/kaniko/executor",
    "--context=$CONTEXT_PATH",
    "--dockerfile=$DOCKERFILE_PATH",
    "--destination=$DOCKER_REGISTRY/$DOCKER_IMAGE:$IMAGE_TAG"]
