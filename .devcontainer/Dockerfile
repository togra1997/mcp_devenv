FROM python
USER root

######################
# MCPサーバーのインストール
WORKDIR /workspace
RUN apt -y update && apt -y upgrade && apt -y install npm
# ファイル操作用のモジュールをインストール
RUN npm install @modelcontextprotocol/server-filesystem
######################
