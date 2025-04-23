ARG PYTHON_VERSION="3.11"
ARG POETRY_VERSION="2.1.1"

FROM mcr.microsoft.com/vscode/devcontainers/python:${PYTHON_VERSION}

RUN apt update && apt install --yes wget graphviz bash-completion
RUN pipx install poetry==${POETRY_VERSION}
RUN pipx inject poetry poetry-dynamic-versioning=="1.7.0"
RUN pipx inject poetry poetry-plugin-export=="1.9.0"
RUN pipx install agentsociety=="1.3.6"

USER vscode

RUN poetry completions bash >> ~/.bash_completion
