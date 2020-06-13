# 【要件】

## vue-cliを用いてプロジェクトが作成されている
以下のコマンドにて、プロジェクトを作成

```bash
% vue create sample-vue-app
```

## ローカルサーバーを起動し、localhostにアクセスすると「Hellow World！！」と表示される
<img src="https://i.gyazo.com/73b9697e62d542314649e12433ed8fe6.png" alt="Image from Gyazo" width="886"/>

App.vueファイルを以下のように編集することで実現しました。
### before

```html
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>
```


### after

```html
<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Hello World！！"/>
  </div>
</template>
```

## App.vue、main.js、index.htmlの役割が理解できている

### main.jsの役割
- Vueオブジェクトを生成している
- index.htmlファイルの`<div id="app"></div>`にApp.vueのHTML文章が読み込まれるように設定している

### App.vueの役割
- ページに表示されているHTML文章はすべてApp.vueファイルの内容
- このファイルを編集することで、ブラウザの表示を変更することができる

### index.htmlの役割
- public/index.htmlファイルはコンパイルされる前の状態、つまり実際に読み込まれるファイルではない
- 実際に読み込まれるファイルは`./dist/index.html`である
- `<div id="app"></div>`の部分に各ページの内容が反映される（main.jsで設定されている）