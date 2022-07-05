# Reactの環境設定
Reactの環境構築を行い、ESLintとPrettierの設定を行いました。

## React環境構築

1. Node.jsのインストール
2. インストールされているかを確認
`node -v`
3. React環境のファイルを作成　
`npx create-react-app react-app`
*react-appは任意のファイル名
4. バージョンの変更(18から17へ)
`npm uninstall react react-dom`
`npminstall(yarn add) react@17.0.2 react-dom@17.0.2`
5. バージョン変更に伴い、index.jsの変更。
```index.js
import React from 'react';
import ReactDOMfrom 'react-dom';
import './index.css';import App from './App';
import reportWebVitalsfrom './reportWebVitals';

ReactDOM.render(
    <React.StrictMode>
    <App />
    </React.StrictMode>,
document.getElementById('root')
);
reportWebVitals();
```
6. App.jsxに
`import React from 'react';`
を追加
7. 作成したファイルへ移動
`cd react-app`
8. ブラウザでファイルを表示
`npm start`
9. http://localhost:3000 でReactのTopページが表示されれば環境構築完了



## ESLintの設定

1. ESLintをインストール
`npm install eslint --save-dev`
2. ESLintのconfigファイルの雛形を作成
`npm init @eslint/config`
3. 対話形式で登録。.eslintrc.jsが作成される



## Prettierの設定
1. prettierをインストール
`npm install --save-dev --save-exact prettier`
2. eslint-config-prettier をインストール
`npm install --save-dev eslint-config-prettier`
3. ESLint の設定ファイルにprettier追記（.eslintrc.js）
4. エラーが出るので、.eslintrc.jsの 「'prettier/react'」をコメントアウト



## VSコードの設定
1. VScodeの拡張機能からESLintとprettierをインストール
2. .vscode →　settings.jsonに設定の記述



### 参考資料
#### npm で React(TypeScript) に ESLint と Prettier を導入
> https://zenn.dev/nakashi94/articles/f67fa9b54437da

#### VS Codeに「Prettier」「ESLint」「Stylelint」を設定して、WEBサイトをコーディング
> https://atelier-light.com/blog/vscode-code-lint-format/
