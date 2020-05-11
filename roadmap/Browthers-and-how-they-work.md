# Browthers and how they work?

[読む](https://www.html5rocks.com/ja/tutorials/internals/howbrowserswork/)

## Browtherの役割
> ユーザーの選択したウェブ リソースをサーバーに要求してブラウザ ウィンドウに表示する

URIでユーザが指定

## メインフロー
レンダリング
![フローイメージ](https://www.html5rocks.com/ja/tutorials/internals/howbrowserswork/flow.png)
> 要求したドキュメントのコンテンツをネットワーキング レイヤから取得

> HTML ドキュメントの解析を開始し、タグを「コンテンツ ツリー」というツリー内の DOM ノードに変換

> 外部の CSS ファイルと style 要素内のスタイル データを解析

> スタイル情報と HTML 内の視覚的な指示を組み合わせて、「レンダー ツリー」という別のツリーが作成

> 「レイアウト」処理に進みます。つまり、画面に表示される正確な座標が各ノードに割り当てられます

> レンダー ツリーが走査され、UI バックエンド レイヤを使用して各ノードが描画されます。


## 構成要素
1. ユーザー インターフェース
2. ブラウザ エンジン
3. レンダリング エンジン
4. ネットワーキング
5. UI バックエンド
6. JavaScript インタープリタ
7. データ ストレージ

## 用語
### DOM
Document Object Model
> HTML ドキュメントや、HTML 要素と JavaScript などの外部世界とのインターフェースをオブジェクトで表現したもの

DOMツリー
![DOMツリーイメージ](https://www.html5rocks.com/ja/tutorials/internals/howbrowserswork/image015.png)

### パーサー
構文解析器
> 解析ツリーを構築する

HTML パーサー
> HTML パーサーの役割は、HTML マークアップを解析して解析ツリーを作成することです。

DTD（Document Type Definition）
堅い文法。HTMLは緩い文法

HTMLのアルゴリズムは
> 「トークン化」と「ツリー構築」の 2 段階で構成

### レキサー
> 入力を有効なトークンに分割する


### レンダリングエンジン
> レンダリング エンジンの仕事は「レンダリング」、つまり、要求されたコンテンツをブラウザの画面に表示することです。


|[Webkit](https://webkit.org/)|Gecko|
|---|---|
| Safari と Chrome | Firefox。Mozilla 用の独自のレンダリング エンジン   |
