# geeksai-2021
はじめてでもわかる！コンテナ入門 - 社内研修公開しちゃいます -
  * https://talent.supporterz.jp/geeksai/2021/

# hands-on
## [002](./002)
### 必須課題 
#### コンテンツのbuild及びrun
ディレクトリ以下のファイルを用いてGolangのコードを動作させましょう。

- 己の http://<myip>:1323 にアクセスしてアクセスを確認しましょう!!! 

```
cd 002
docker build -t webweb:v1 .
docker run -p 1323:1323 -t webweb:v1
```


#### 挑戦課題
- [マルチステージビルド](https://matsuand.github.io/docs.docker.jp.onthefly/develop/develop-images/multistage-build/) について調べて対応してください。

