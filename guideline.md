# コーディングガイドライン

## 目次
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [コーディングガイドライン](#コーディングガイドライン)
  - [目次](#目次)
  - [全体で共通の規約](#全体で共通の規約)
    - [プロトコル](#プロトコル)
    - [エンコーディング](#エンコーディング)
    - [インデント](#インデント)
  - [HTMLコーディング規約](#htmlコーディング規約)
    - [文書型宣言](#文書型宣言)
    - [文書の言語](#文書の言語)
    - [スタイルシートとスクリプトの属性の省略](#スタイルシートとスクリプトの属性の省略)
    - [引用符](#引用符)
    - [void要素のスラッシュ](#void要素のスラッシュ)
  - [一般的な書式ルール](#一般的な書式ルール)
    - [インデント](#インデント-1)
    - [大文字/小文字](#大文字小文字)
    - [文末のスペース](#文末のスペース)

<!-- /code_chunk_output -->

## 参考にしたサイト
> [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)
  [YngLabコーディング規約](https://github.com/YngLab/coding_rule?tab=readme-ov-file)
  [Markdown記法 チートシート](https://qiita.com/Qiita/items/c686397e4a0f4f11683d)

## 全体で共通の規約
### プロトコル
```html
<!-- NG -->
<script src="http://www.google.com/js/gweb/analytics/autotrack.js"></script>
<!-- 非推奨-->
<script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
<!-- 推奨 -->
<script src="https://www.google.com/js/gweb/analytics/autotrack.js"></script>
```

### エンコーディング
ソースコードのエンコードは UTF-8(BOMなし) を使用する。

### インデント
スペースを2つ使う。
```html
<!-- 非推奨 -->
<ul>
    <li>A...
    <li>B...
</ul>
<!-- 推奨 -->
<ul>
  <li>A...
  <li>B...
</ul>
```

## HTMLコーディング規約
### 文書型宣言
HTML5の文書型宣言を使ってください。
```html
<!DOCTYPE html>
```

### 文書の言語
```<html>```要素に lang 属性を使い、文書の言語を設定してください。
```html
<html lang="ja"></html>
```

### スタイルシートとスクリプトの属性の省略
typeは自動認識されるため記述しない。
```html
<!-- 非推奨 -->
<link rel="stylesheet" href="style.css" type="text/css">
<script src="smoothscroll.js" type="text/javascript"></script>

<!-- 推奨 -->
<link rel="stylesheet" href="style.css">
<script src="smoothscroll.js"></script>
```

### 引用符
ダブルクオーテーションを使用する
```html
<!-- 非推奨 -->
<a class='btn-submit'>送信</a>

<!-- 推奨 -->
<a class="btn-submit">送信</a>
```

### void要素のスラッシュ
現在のHTMLの仕様(HTML Living Standard)において、HTMLタグの最後のスラッシュは不要となっております。
> 参考→ https://oopsoop.com/trailing-slash-on-void-elements/
```html
<!-- 非推奨 -->
<img src="logo.png" alt="ロゴ" />
<!-- 推奨 -->
<img src="logo.png" alt="ロゴ">
```

## 一般的な書式ルール
### インデント
半角スペース2つ分もしくはTabでインデントする。Tabとスペースを混在させない。
```html
<!-- OK -->
<ul>
  <li>Great
  <li>Great
</ul>
<!-- OK -->
<ul>
　　　<li>Great
　　　<li>Great
</ul>

<!-- NG -->
<ul>
　　　<li>Great
  <li>Great
</ul>
```

### 大文字/小文字
すべて小文字のみ使用する。(名称のテキストは除く)
```html
<!-- NG -->
<IMG src="logo.png" alt="East">
<!-- OK -->
<img src="logo.png" alt="East">
```

### 文末のスペース
```html
<!-- NG -->
<p>テキストが入ります_
<!-- OK -->
<p>キストが入ります
```
