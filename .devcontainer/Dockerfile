ARG VARIANT="1.17-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/go:0-${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends git

USER vscode
RUN go get -u github.com/cosmtrek/air && \
    go build -o /go/bin/air github.com/cosmtrek/air

RUN go install golang.org/x/tools/gopls@latest
RUN go install golang.org/x/lint/golint@latest
RUN go install github.com/josharian/impl@latest

# COPY go.mod go.mod
# COPY go.sum go.sum
# RUN go mod download

CMD ["air", "-c", ".air.toml"]