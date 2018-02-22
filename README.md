# node-red-translationapp

テンプレートノードに記述するHTMLコードです。
特に凝ったスタイルのしていない、画面デザインの一例ですので、お好みで変更ください。

### 初期表示画面のHTML
```
<h1>Watson Translation App</h1>
<H2>翻訳したい文章を英語で入力して下さい</H2>
※英語から日本語への翻訳になります。
<form action="/translate" method="post">
    <textarea name="inputtext" cols="50" rows="10"></textarea>
    <br>
    <input type="submit" value="翻訳する"/>
</form>
```

### 翻訳後表示画面のHTML
```
<h1>Watson Translation App</h1>
<H2>翻訳したい文章を英語で入力して下さい</H2>
※英語から日本語への翻訳になります。
<form action="/translate" method="post">
    <textarea name="inputtext" cols="50" rows="10">{{payload}}</textarea>
    <br>
    <input type="submit" value="翻訳する"/>
</form>
```
