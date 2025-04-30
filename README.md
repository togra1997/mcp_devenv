# MCP サーバープロジェクト

このリポジトリは、Model Context Protocol (MCP) サーバーを使用したプロジェクトです。MCPを活用して、モデルにコンテキストを提供するための様々なサーバーが設定されています。

## 概要

Model Context Protocol (MCP) は、AI モデルに対して様々な種類のコンテキストを提供するためのプロトコルです。このプロジェクトでは、以下のMCPサーバーを設定しています：

- **filesystem**: ファイルシステムへのアクセスを提供
- **fetch**: ウェブからのデータ取得機能を提供
- **git**: Gitリポジトリとの連携機能を提供
- **time**: 時間関連の機能を提供
- **sequential-thinking**: 段階的な思考プロセスを支援する機能を提供

## 環境構築

このプロジェクトは開発コンテナ（Dev Container）を使用して環境を構築しています。Docker環境が必要です。

```bash
# 開発コンテナを起動
code .
# VSCode上で「Reopen in Container」を選択
```

開発コンテナには以下の環境が含まれています：
- Python
- Node.js (npm)
- uv パッケージマネージャ

## 使用方法

1. VSCodeでプロジェクトを開きます
2. 「Reopen in Container」を選択して開発コンテナ内で作業します
3. MCPサーバーの設定は `.vscode/mcp.json` で管理されています

## MCPサーバーについて

各MCPサーバーは特定のタスクを担当しています：

### filesystem サーバー

ファイルシステムへのアクセスを提供します。

```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-filesystem", "/workspace"],
  "env": {}
}
```

### fetch サーバー

ウェブからデータを取得する機能を提供します。

```json
{
  "command": "uvx",
  "args": ["mcp-server-fetch"]
}
```

### git サーバー

Gitリポジトリとの連携機能を提供します。

```json
{
  "command": "uvx",
  "args": ["mcp-server-git", "--repository", "path/to/git/repo"]
}
```

### time サーバー

時間関連の機能を提供します。

```json
{
  "command": "uvx",
  "args": ["mcp-server-time"]
}
```

### sequential-thinking サーバー

段階的な思考プロセスを支援する機能を提供します。

```json
{
  "command": "npx",
  "args": ["-y", "@modelcontextprotocol/server-sequential-thinking"]
}
```

## ライセンス

このプロジェクトは<b>MITライセンス</b>の下で公開されています。
