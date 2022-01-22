# data-normalizers

データの正規化ライブラリ等を収集します。
プルリク大歓迎です。

## 文字コード

- [uconv](https://github.com/unicode-org/icu/tree/main/icu4c/source/extra/uconv)([wikipedia](https://en.wikipedia.org/wiki/Uconv),[library document](https://unicode-org.github.io/icu/))
  - The uconv command is an iconv(1)-like conversion / transcoding program.
  - 色々な変換が可能
    - `uconv -f utf-8 -t utf-8 -x --remove-signature '::nfkc;'` BOM を削除し NFKC で unicode 正規化

## 住所

- (ja) [geolonia/normalize-japanese-addresses](https://github.com/geolonia/normalize-japanese-addresses)
  - オープンソースの住所正規化ライブラリ。
  - 経産省の [IMI コンポーネントツール](https://info.gbiz.go.jp/tools/imi_tools/)のジオコーディングの仕組みからインスピレーションをうけて開発された。

## 電話番号

- () [google/libphonenumber](https://github.com/google/libphonenumber)
  - Google's common Java, C++ and JavaScript library for parsing, formatting, and validating international phone numbers. The Java version is optimized for running on smartphones, and is used by the Android framework since 4.0 (Ice Cream Sandwich).
