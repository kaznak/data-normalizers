# data-normalizers

データのコードや正規化ライブラリ等を収集します。
プルリク大歓迎です。

## ライブラリ

### [uconv](https://github.com/unicode-org/icu/tree/main/icu4c/source/extra/uconv)([wikipedia](https://en.wikipedia.org/wiki/Uconv),[library document](https://unicode-org.github.io/icu/))
- 対象: charcode
- The uconv command is an iconv(1)-like conversion / transcoding program.
- 色々な変換が可能
  - `uconv -f utf-8 -t utf-8 -x --remove-signature '::nfkc;'` BOM を削除し NFKC で unicode 正規化
  - `echo -e "あいうえお\nカキクケコ" | uconv -x latin` かなをローマ字化
  - `echo -e "あいうえお\nカキクケコ" | uconv -x hiragana-latin` ひらがなのみをローマ字化
  - `echo -e "あいうえお\nカキクケコ" | uconv -x katakana-latin` カタカナのみをローマ字化

### [geolonia/normalize-japanese-addresses](https://github.com/geolonia/normalize-japanese-addresses)
- 対象: addr.ja
- オープンソースの住所正規化ライブラリ。
- 経産省の [IMI コンポーネントツール](https://info.gbiz.go.jp/tools/imi_tools/)のジオコーディングの仕組みからインスピレーションをうけて開発された。
- [総務省からダウンロードできる全国地方公共団体コード コード一覧表](#都道府県コード--地方公共団体コードwikipedia)とは、住所の表記の仕方が異なるため、これを使用する場合地方公共団体コードテーブルの正規化が必要。

- 関連:
  - [kaznak/normalize-japanese-addresses-cli](https://github.com/kaznak/normalize-japanese-addresses-cli)([npm](https://www.npmjs.com/package/normalize-japanese-addresses-cli))

### [google/libphonenumber](https://github.com/google/libphonenumber)
- 対象: tel.ja
- Google's common Java, C++ and JavaScript library for parsing, formatting, and validating international phone numbers. The Java version is optimized for running on smartphones, and is used by the Android framework since 4.0 (Ice Cream Sandwich).

### [reacherhq/check-if-email-exists](https://github.com/reacherhq/check-if-email-exists)
- 対象: email
- Check if an email address exists without sending any email, written in Rust.
- license: AGPL, comercial

## コード

### 都道府県コード / 地方公共団体コード([wikipedia](https://ja.wikipedia.org/wiki/%E5%85%A8%E5%9B%BD%E5%9C%B0%E6%96%B9%E5%85%AC%E5%85%B1%E5%9B%A3%E4%BD%93%E3%82%B3%E3%83%BC%E3%83%89))
- 対象: addr.ja
- サイト: [全国地方公共団体コード コード一覧表](https://www.soumu.go.jp/denshijiti/code.html)
