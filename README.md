# poetry

This is a Docker image based on Python that installs Poetry on top.

It provides a convenient environment for managing Python projects with Poetry.

## Available tags

Tags reflect the image of python used and the version of poetry installed on top.

Tags follow this format : `${POETRY_VERSION}-python${PYTHON_TAG}`.

Currently, `latest` corresponds to `1.8-python3.12-slim`.

Here are the TAGS currently available :
```Python
POETRY_VERSIONS = ["1.6", "1.7", "1.8"]
PYTHON_VERSIONS = ["3.8", "3.9", "3.10", "3.11", "3.12"]
PYTHON_TYPES = ["", "-slim"]
```

Other tags will be added later.

## Clone repository

To clone the github repository containing the Dockerfile used, follow these steps :

1. Clone the repository:
    ```bash
    git clone https://github.com/bouajajais/poetry.git
    ```

2. Navigate to the project directory:
    ```bash
    cd poetry
    ```

2. Build the Docker image using the provided Dockerfile:
    ```bash
    docker build -t poetry .
    ```

    The `docker build` command accepts the following arguments:
    - `ARG PYTHON_TAG=3.12-slim`: The Python base image tag.
    - `ARG POETRY_VERSION=1.8.*`: The Poetry version to install.
    - `ARG PYTHONDONTWRITEBYTECODE=1`: Other argument.
    - `ARG PYTHONUNBUFFERED=1`: Other argument.

3. Run the Docker container:
    ```bash
    docker run --rm -it poetry bash
    ```

## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.