ARG VARIANT="1.17-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/go:0-${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends git vim

USER vscode
RUN go get -u github.com/cosmtrek/air && \
    go build -o /go/bin/air github.com/cosmtrek/air

RUN go install golang.org/x/tools/gopls@latest
RUN go install golang.org/x/lint/golint@latest
RUN go install github.com/josharian/impl@latest

CMD ["air", "-c", ".air.toml"]