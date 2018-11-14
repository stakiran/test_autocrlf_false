# autocrlf=false の時

つくる

```
$ git config --local core.autocrlf false

$ crlf.txt
CRLF のテキストファイルをつくる

$ lf.txt
LF のテキストファイルをつくる

$ git add -A
$ git commit -m "a"
$ git push
```

別ディレクトリで clone してみる

