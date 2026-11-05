# font-lxgw-wenkai-tc

霞鶩文楷 TC 的 woff2 webfont，子集化後僅含 CJ（中日）字符（移除韓文以縮小檔案）。供 jsDelivr CDN 直接引用。另附 Regular 的 ttf，給讀不了 woff2 的程式用，例如在瀏覽器裡跑的 ManimGX（它用 Typst 排版）。

- **來源**：[lxgw/LxgwWenkaiTC](https://github.com/lxgw/LxgwWenkaiTC) `v1.522`
- **授權**：SIL Open Font License 1.1（見 `OFL.txt`）
- **建置**：fonttools `pyftsubset --flavor=woff2 --with-zopfli`、移除 Hangul codepoints；ttf 是把 Regular 的 woff2 用 fonttools 解回 ttf，字符和 woff2 相同

## 檔案

- `LXGWWenKaiTC-Medium.woff2` (5.7M)
- `LXGWWenKaiTC-Regular.woff2` (5.1M)
- `LXGWWenKaiTC-Regular.ttf` (14M)：同一份字符，未壓縮。網頁的 `@font-face` 請用 woff2。

## CDN 用法

```css
@font-face {
  font-family: "LXGWWenKaiTC";
  font-weight: 500;
  font-display: swap;
  src: url("https://cdn.jsdelivr.net/gh/yelban/font-lxgw-wenkai-tc@v1.0.0/LXGWWenKaiTC-Medium.woff2") format("woff2");
}

@font-face {
  font-family: "LXGWWenKaiTC";
  font-weight: 400;
  font-display: swap;
  src: url("https://cdn.jsdelivr.net/gh/yelban/font-lxgw-wenkai-tc@v1.0.0/LXGWWenKaiTC-Regular.woff2") format("woff2");
}
```

ttf 從 `v1.1.0` 起才有：

```
https://cdn.jsdelivr.net/gh/yelban/font-lxgw-wenkai-tc@v1.1.0/LXGWWenKaiTC-Regular.ttf
```

## 字符範圍

**保留**：ASCII / Latin Extended / 一般標點 / 通用符號 / 平假名 / 片假名 / CJK 統一漢字（含 Ext A/B/C/D/E/F/I）/ CJK 相容字 / 全形半形（去韓文段）

**排除**：Hangul Jamo / Hangul Syllables（U+1100-11FF, U+3130-318F, U+A960-A97F, U+AC00-D7AF, U+D7B0-D7FF, U+FFA0-FFDC）

## 版本對應

| 此 repo tag | 對應上游版本 | 變更 |
|---|---|---|
| v1.0.0 | v1.522 | 初版 |
| v1.1.0 | v1.522 | 加 Regular 的 ttf；woff2 不變 |
