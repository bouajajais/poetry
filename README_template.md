# poetry

This Docker image is built on top of the `{BASE_IMAGE}` image.

It installs the following element(s) on top:

{INSTALLED_FEATURES}

## Available tags

Tags reflect the image of python used and the version of poetry installed on top.

Tags follow this format : `{TAG_FORMAT}`.

Currently, `latest` corresponds to `{DEFAULT_TAG}`.

Other tags will be added later.

## Dockerhub

These images can be found in Dockerhub through the following link:

[https://hub.docker.com/repository/docker/{DOCKERHUB_USERNAME}/{IMAGE_NAME}/general](https://hub.docker.com/repository/docker/{DOCKERHUB_USERNAME}/{IMAGE_NAME}/general)

## Clone repository

To clone the github repository containing the Dockerfile used, follow these steps :

1. Clone the repository:
    ```bash
    git clone [https://github.com/{GITHUB_USERNAME}/{IMAGE_NAME}.git](https://github.com/{GITHUB_USERNAME}/{IMAGE_NAME}.git)
    ```

2. Navigate to the project directory:
    ```bash
    cd {IMAGE_NAME}
    ```

2. Build the Docker image using the provided Dockerfile:
    ```bash
    docker build -t {IMAGE_NAME} .
    ```

    The `docker build` command accepts the following arguments:
    - `ARG PYTHON_TAG={LATEST_PYTHON_TAG}`: The Python base image tag.
    - `ARG POETRY_VERSION={LATEST_POETRY_VERSION}.*`: The Poetry version to install.
    - `ARG PYTHONDONTWRITEBYTECODE=1`: Other argument.
    - `ARG PYTHONUNBUFFERED=1`: Other argument.

3. Run the Docker container:
    ```bash
    docker run --rm -it {IMAGE_NAME} bash
    ```

## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.