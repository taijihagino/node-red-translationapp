# node-red-translationapp

## 各ノードの説明です

### パラメーター確認
ノードの種類: Switch
```
Property: msg.payload.inputtext
is null   -> 1
otherwise -> 2
```

### パラメーター加工
ノードの種類: Function
```
msg.payload = msg.payload.inputtext;
return msg;
```

### Language Translator API呼び出し
ノードの種類: Language Translator
```
Mode: Translate
Domain: News
Source to Target: English to Japanese
```

### 初期表示画面のHTML
ノードの種類: Template
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
ノードの種類: Template
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
テンプレートノードに記述するHTMLコードは、特に凝ったスタイルにしていない、画面デザインの一例ですので、お好みで変更ください。
