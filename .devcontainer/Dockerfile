FROM python
USER root

######################
# MCPサーバーのインストール
WORKDIR /workdir
RUN apt -y update && apt -y upgrade && apt -y install npm
# ファイル操作用のモジュールをインストール
RUN npm install @modelcontextprotocol/server-filesystem
######################
