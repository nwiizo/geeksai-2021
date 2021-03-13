# geeksai-2021
はじめてでもわかる！コンテナ入門 - 社内研修公開しちゃいます -
  * https://talent.supporterz.jp/geeksai/2021/

# hands-on
## 001
### 必須課題
- nginx を動作させてやってブラウザアクセスして確認しましょう
```
docker run -it --rm -d -p 8080:80 --name web nginx
```
#### 挑戦課題
- /usr/share/nginx/html を変更してページを変更してください。方法は問いません。

## [002](./002)
### 必須課題 
#### コンテンツのbuild及びrun
ディレクトリ以下のファイルを用いてGolangのコードを動作させましょう。

- http://<myip>:1323 にブラウザアクセスして確認しましょう!!! 

```
cd 002
docker build -t webweb:v1 .
docker run -p 1323:1323 -t webweb:v1
```


#### 挑戦課題
- [マルチステージビルド](https://matsuand.github.io/docs.docker.jp.onthefly/develop/develop-images/multistage-build/) について調べて対応してください。


### 003 
本当に申し訳ございません。用意してないので自分の開発環境をDocker化していってください。質問は無限にOkです。ここまで来た人は実質弟子なので[Twitter](https://twitter.com/nwiizo) にでも質問してください、

