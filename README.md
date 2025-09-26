## 初めに
今更ですが、よく使うSassの関数やMixinなどをまとめたリポジトリです。  
最近、あの関数はどこだっけ、みたいなのが多くなってきたので、まとめてみたのが経緯です。    
基本的にはSassのコンパイラと整形ツールにはパッケージをインストールせず、VSCodeの拡張機能だけでコンパイル&整形できる運用を想定しています。

---

## ディレクトリ構成
```
├── .gitignore              # github除外設定
├── README.md               # このファイル
├── .vscode/                # VSCode設定
│   ├── settings.json
│   └── csscomb.json
├── assets/
│   ├── css/                # コンパイル済みのCSS
│   │   ├── aspect-ratio.css
│   │   ├── container-query.css
│   │   ├── fluid-size.css
│   │   ├── font-face.css
│   │   ├── hover.css
│   │   ├── leading-trim.css
│   │   ├── line-height.css
│   │   ├── media-query.css
│   │   ├── responsive-size.css
│   │   ├── space-loop.css
│   │   ├── utility.css
│   │   ├── visually-hidden.css
│   │   └── zero-space.css
│   ├── fonts/              # フォントファイル
│   │   ├── Test-Bold.otf
│   │   ├── Test-Bold.woff
│   │   ├── Test-Bold.woff2
│   │   ├── Test-Regular.otf
│   │   ├── Test-Regular.woff
│   │   └── Test-Regular.woff2
│   ├── images/             # 画像ファイル
│   │   ├── test.avif
│   │   ├── test.gif
│   │   ├── test.jpg
│   │   └── test.png
│   └── sass/               # Sass/SCSSファイル
│       ├── _function.scss      # 関数定義
│       ├── _mixin.scss         # 主要mixin集
│       ├── _variable.scss      # デザイン変数・ブレークポイント
│       ├── _index.scss         # ここの@forwardで転送
│       ├── aspect-ratio.scss
│       ├── container-query.scss
│       ├── fluid-size.scss
│       ├── font-face.scss
│       ├── hover.scss
│       ├── leading-trim.scss
│       ├── line-height.scss
│       ├── media-query.scss
│       ├── responsive-size.scss
│       ├── space-loop.scss
│       ├── utility.scss
│       ├── visually-hidden.scss
│       └── zero-space.scss
```

## 必須VSCodeプラグイン
- [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=glenn2223.live-sass)（Sass→CSS即時コンパイル）

## 推奨VSCodeプラグイン
- [CSSComb](https://marketplace.visualstudio.com/items?itemName=naumstory.vscode-csscomb)（CSS/Sass整形）

## 使い方
- `sass/`配下の各`.scss`ファイルでmixinや関数を呼び出し、`css/`にコンパイル。
- 主要mixin/関数の使い方は各ファイルのSassDocコメント・サンプルコード参照。
- VSCodeでLive Sass Compilerを有効化し、保存時に自動コンパイル。

## 説明
- 各関数名、mixin名で`◯◯.scss`を作成して`css`にコンパイルしています。

---

## 最後に
Sassをコンパイルできるようであれば、どのようなツールでも構いません。  
目的は、簡単に確認することが目的ですので、必須プラグインとして`Live Sass Compiler`を指定させていただきました。
