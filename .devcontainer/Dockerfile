FROM python
USER root

######################
# MCPサーバーのインストール
WORKDIR /workspace
# サーバーで必要な環境をインストール(npm uv など)
RUN apt -y update && apt -y upgrade && apt -y install npm
######################
