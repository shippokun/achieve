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

## 柔軟な背景の位置指定

- background-position
- background-origin: content-box;
- calc()

## ストライプ模様の背景

- background: linear-gradient();
  - カラーストップの位置をまったく同じ位置にするとストライプを表現できる（それぞれ異なる値だとグラデーションを表現）
  - `background-size: 100% Xpx;` で繰り返し表示できる
- 縦のストライプ、斜めのストライプ

# 4章：視覚効果

## 単方向の影

# 5章：タイポグラフィー

- `hyphens: auto;`
  - ハイフネーション
