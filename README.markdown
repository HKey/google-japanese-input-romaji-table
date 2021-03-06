Google日本語入力用ローマ字テーブル
====


[yuzuemon/google-japanese-input-romaji-table](https://github.com/yuzuemon/google-japanese-input-romaji-table)の`dvorakjp-.txt`を修正・拡張したローマ字テーブルです。


内容
----

*  dvorakjp-edited.txt - DvorakJP-配列用のローマ字テーブル修正拡張版（英語キーボード用）

使い方
----

Google日本語入力の環境設定ダイアログを開き、ローマ字テーブルのカスタマイズボタンを押して、編集ボタンの「ファイルからインポート」を選び、`dvorakjp-edited.txt`を読み込みます。


`dvorakjp-edited.txt`について
----
`dvorakjp-edited.txt`は`dvorakjp-.txt`を土台に次のような変更を施しました。


`dvorakjp-edited.txt`では、QWERTY配列の感覚のまま矢印キーを入力できるようになります。

### `ch*`キー配置の追加

`ch`から始まるキーについて、「ちゃ、ち、ちゅ、ちぇ、ちょ」はありましたが、二重母音・撥音拡張が見当たらなかったため、次のキーマップを追加しました。

    ch' ちゃい
    ch, ちょう
    ch. ちぇい
    ch; ちゃん
    chj ちぇん
    chp ちゅう
    chq ちょん
    chk ちゅん
    chx ちぃん

### `th*`及び`tn*`の修正
http://www7.plala.or.jp/dvorakjp/ では、`t`キーとのコンビネーションキーは`n`です。

`dvorakjp-.txt`を見ると、どうも`th*`と`tn*`の使い方が混ざっているように見えたので、`th*`から始まるキー配置は「てゃ、てゅ」等へ、`tn*`から始まるキー配置は`ch*`と同等に変更しました。

また、もともと`th*`に配置されていた「てょん」や「てぇん」は、日本語的に成立し得ない言葉だと思い削除することにしました。  
※ただし「てぃん」のみ残留

#### `th*`

    thx てぃん

#### `tn*`

    - tn' てゃい
    - tn. てぇい
    - tn; てゃん
    - tnj てぇん
    - tnk てゅん
    - tnp てゅう
    - tnq てょん
    - tnx てぃん
    + tn' ちゃい
    + tn. ちぇい
    + tn; ちゃん
    + tnj ちぇん
    + tnk ちゅん
    + tnp ちゅう
    + tnq ちょん
    + tnx ちぃん

### `yp`キー配置の追加

`yp`→「ゆう」と変換できるようにしました。

### 「ん」と「っ」

それぞれ単体で変換できるようにしました。

    ; っ
    q ん

これに伴って`;`と`q`から始まる組み合わせを削除しました。

    - ;h ←
    - ;t ↓
    - ;n ↑
    - ;s →
    - ;- 〜
    - ;[ 『
    - ;] 』
    - qa くぁ
    - qe くぇ
    - qi くぃ
    - qo くぉ
    - qq っ q
    - qu く
