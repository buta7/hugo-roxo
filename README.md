# README

## セットアップ

サイト作成

```shell
hugo new site hugo-roxo
```

レポジトリ初期化

```shell
cd hugo-roxo
git init
echo '*.bak' >> .gitignore
echo '*~' >> .gitignore
echo '*.orig' >> .gitignore
echo 'public' >> .gitignore
```

テーマ設定

```shell
cd themes 
git submodule add git@github.com:StaticMania/roxo-hugo.git
```

サイト設定

```shell
cd hugo-roxo
cp -pr ./themes/roxo-hugo/exampleSite/{config.toml,content,static} .
```

config.toml

```toml
baseURL = "https://higebobo.github.io/hugo-roxo/"
languageCode = "ja"
title = "Hugo Roxo"
theme = "roxo-hugo"
publishDir = "docs"
```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

Githubレポジトリ作成後

```shell
git remote add origin git@github.com:higebobo/hugo-roxo.git
cp somplace/{Makefile,deploy.sh} .
make deploy
```

Github>Settings>Gighub Pages>Source>master branch/docs folder

## 既存のレポジトリからクローンする場合

```shell
git clone git@github.com:higebobo/hugo-roxo.git higebobo-roxo
cd higebobo-roxo
git submodule update --init --recursive
```

## 使い方

### 投稿

新規投稿

```shell
hugo new blog/hello.md
content/blog/hello.md created
```

編集

```shell
vi content/blog/hello.md
```

## Link

* [Roxo Hugo \| Hugo Themes](https://themes.gohugo.io/roxo-hugo/)
