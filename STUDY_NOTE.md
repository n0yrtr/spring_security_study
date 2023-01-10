

# 1.0.0

## やったこと
- 下記の設定値でSpirng Initirizrにてプロジェクトを作成 
![](./README_IMAGES/Spring_Initializr.png)

- ビルドすると、thymeleaf-extras-spirngsecurity6:3.1.0.RELEASEが解決出来ないgradleエラーがでたので、:3.1.1.RELEASEを指定して解決。  
[参考](https://stackoverflow.com/questions/74603629/could-not-resolve-org-thymeleaf-extrasthymeleaf-extras-springsecurity63-1-0-r/74610296)  
理由はよくわかってないがbomの情報が古い？

- bootrunで無事起動(デフォルトのログインページが表示された)

  ![](v1.0.0bootrun.png)



## 疑問点
### 表示されたログインページはどこにある？
該当のHTMLを直接いじることは出来ないのか？とちょっと思った。

### ライブラリを入れるだけで、ログインページの表示まで行われるのはなぜか。
普通のライブラリは、入れても使わなければ意味がない。  
ただSpringSecurityは入れるだけで、ログインページの表示まで行われた。  
SpringStartar系のライブラリはSpringへの組込みまで行われるがそれと同じ理屈か。  
どちらにしてもSpringStartarとしてのライブラリがどのようにして作っているかわからないので、  
そこから調べてみたい。

### maven bom の仕組みをちゃんとわかっていないので、エラー解決はしたが、何が直されるとこの問題は発生しなくなるのかはわかっていない。
maven bomにて同じライブラリ群のバージョン合わせをしているが、 
今回のエラーはどうして起こっているのか？公式がbom登録の更新をしていないとかそういうなのか？  	