# CSSシークレット ―47のテクニックでCSSを自在に操る

https://www.amazon.co.jp/dp/4873117666

# 2章：背景とボーダー

## 半透明なボーダー

半透明なborderを使うと、背景色がボーダーにまで侵食してしまう。
`background-clip: padding-box;` を使うことで背景とボーダーが重ならないようになる。

```css
border: 10px solid hsla(0, 0%, 100%, .5);
background: white;
// ↑ この状態では border にも white が入ってしまう

background-clip: padding-box;
```

## 複数のボーダー

- box-shadow で再現する
  - 要素の外側に疑似的なボーダーを表示しているだけなので、ホバーやクリックなどのマウスイベントは発生しない。
  - 発生させたい場合は、inset を指定して、要素の内側に描画されるようにする。追加のpaddingは必要。
- outline で再現する

