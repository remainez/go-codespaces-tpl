# go-codespaces-tpl

## Introduction

This is a pretty cool golang template for GitHub Codespaces.

[JP] イケてるGitHub Codespaces用Goテンプレートです。

## Prerequisites

* You must have the right to participate in the beta testing of GitHub Codespaces.
* [JP] GitHub Codespacesのベータテスト参加権を取得している必要があります

## Usage

1. Click [Use this template](https://github.com/remainez/go-codespaces-tpl/generate)
2. Navigate to the main page of the newly created repository. Under the repository name, use the `<>Code` drop-down menu, and in the `Codespaces` tab, click `Create codespace on main`.
3. Wait for the container to be activated by spinning a [hand spinner](https://g.co/kgs/ZDRQRJ).
4. Once launched, type the following command in the terminal tab.
```bash
$ air -c .air.toml
```
5. If Air starts and the console displays "Hello World", it is successful.

## Usage [JP]

1. [Use this template](https://github.com/remainez/go-codespaces-tpl/generate) をクリックし、新しいリポジトリを作成します。
2. 新しく作成されたリポジトリのメインページに遷移し、リポジトリ名の下にある `<>Code` のドロップダウンから `Codespaces` タブを開き、`Create codespace on main`をクリックします。
3. [hand spinner](https://g.co/kgs/ZDRQRJ) でも回しながら、コンテナが起動するのを待ちます。
4. 起動したらターミナルタブから下記コマンドを実行します。
```bash
$ air -c .air.toml
```
5. Airが起動し、コンソールに "Hello World" と表示されたら成功です。

## Environment

- Base image
  - [mcr.microsoft.com/vscode/devcontainers/go:0-1.17-bullseye](https://hub.docker.com/_/microsoft-vscode-devcontainers)
- Framework
  - [gin-gonic/gin](https://github.com/gin-gonic/gin)
- Live reload utility 
  - [cosmtrek/air](https://github.com/cosmtrek/air)
- Language server
  - [golang/tools/gopls](https://github.com/golang/tools)
- Linter
  - [golang/lint](https://github.com/golang/lint)
- Others
  - [impl](https://github.com/josharian/impl) 
