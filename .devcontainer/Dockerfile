FROM python
USER root

######################
# MCPサーバーのインストール
WORKDIR /workspace
# サーバーで必要な環境をインストール(npm)
RUN apt -y update && apt -y upgrade && apt -y install npm
# サーバーで必要な環境をインストール(uv)
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/
######################
