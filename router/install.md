# 安裝
在cmd或Terminal進入專案資料夾並輸入以下指令。反正基本上都會使用到，創建完專案資料夾就順便安裝一下router。
```
npm install vue-router
```
安裝完成之後要開始設定各種畫面的路徑，在`src`底下建立`router`資料夾專門用來放置路由相關的.js檔。並新增`index.js`設定路徑。  

首先需要使用`import`導入`Vue`以及`vue-router`，並設定使用`Router`。
```js
// index.js

import Vue from 'vue';
import Router from 'vue-router';

Vue.use(Router);

const routes = [
    // 裡面放要設定的路徑
];

const router = new Router({
    routes
});

export default router;
```
接下來只要把`<router-view />`放入入口網頁，入口網頁就是掛載在h的組件(h也等於cteateElement)，下面範例為"App.vue"。等待[動態路由匹配](https://github.com/PeggyHsiao/Vue-Note/blob/master/router/settingRoute.md)完成就可以開開心心的使用路由切換網頁畫面了。
```js
// main.js

import router from '@/router/index';

new Vue({
  render: h => h(App),
  router,
}).$mount('#app')
```