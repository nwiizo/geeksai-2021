# geeksai-2021
はじめてでもわかる！コンテナ入門 - 社内研修公開しちゃいます -
  * https://talent.supporterz.jp/geeksai/2021/

# hands-on
## 001
main.go
```
package main

import (
  "fmt"
  "net/http"
  "os"
)

func main(){
  http.HandleFunc("/", handler)
  http.ListenAndServe(":8080", nil)
}

func handler(w http.ResponseWriter, r *http.Request){
  msg := os.Getenv("ENENENVVV")
  fmt.Fprintf(w, msg)
}
```

```
FROM golang:latest AS builder

WORKDIR /work
COPY main.go .
RUN go build -o web .

FROM alpine

WORKDIR /exec
COPY --from=builder /work/web .
CMD ["./web"]
```


build
```
docker build -t webweb:v1 .
```
