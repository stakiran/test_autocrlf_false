# autocrlf=false の時
結論:

- 元々やりたかったのは「Download ZIP 時に LF にするのやめて」だった
- できた？
  - できた
  - **autocrlf=false にしてから crlf をコミットする** こと


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

Download ZIP で覗いてみる

- crlf.txt → **CRLF のまま** / false だからコミット時に crlf でも lf にならない。
- lf.txt → LF

意図通り。

別ディレクトリで clone してみる。

- global の autocrlf は true
  - crlf.txt → CRLF
  - lf.txt → **CRLF になっている** / true の動作どおり。
