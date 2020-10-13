vue-cli 學習筆記
===

###### tags: `技術`
20201011

## 資源

[官方文件](https://cli.vuejs.org/guide/installation.html)

[Vue CLI 3 安裝與使用教學](https://www.footmark.info/programming-language/vuejs/vue-cli3-seting/)

## 名詞

新版叫做 "@vue/cli" 舊版 "vue-cli"

快速建好vue開發環境的工具，讓工程師可以專注在開發上，不用去調環境設定就弄個一兩天

### 優點

* 預設好的webpack基本設定
* 一些可選的官方建議套件(e.g. ESLint)
* 還可以用GUI創建專案

---

## 機制

### 1.安裝

```$ npm install -g @vue/cli```


### 2.使用

### 2-1 簡單原型(單一vue檔)

> 這種狀況更建議直接使用線上編輯器 
> [jsbin](https://jsbin.com/fobejut/3/edit?html,js,output)

#### 1. 需要額外安裝

```$ npm install -g @vue/cli-service-global```

#### 2. 建一個專案資料夾，建立單一的vue檔

project/app.vue

 > 只能是這幾種檔名 main.js, index.js, App.vue or app.vue

```
<template>
    <h1>{{title}}</h1>
</template>

<script>
export default {
    name: "myPage",
    data(){
        return {
            title: 'Hi single Vue'
        }
    }
};
</script>
```

#### 3. 啟動開發sever

```$ vue serve```

> 如果localhost顯示可以試試看(或者開無痕):<br/>
>  https://localhost:8080 -> http://localhost:8080

 就可以開始編寫程式囉

#### 4. 打包成上線檔案

```$ vue build```

> 預設會在 /dist 底下


### 2-2 建立一個專案

#### 1. 建立專案

```$ vue create lab ```

![](https://i.imgur.com/OOdsOkh.png)

> lab 是專案的名稱

> Default 跟 Manually的差異:<br/>
> Manually 可以選更多套件(e.g. router)，適合是較大型的專案

![](https://i.imgur.com/YNZXbF0.png)


全部的設定大概長這樣
[可以參考這邊](https://www.footmark.info/programming-language/vuejs/vue-cli3-seting/)

![](https://i.imgur.com/oaTt1Gf.png)


#### 2. 進入專案

```$ cd lab ```

#### 3. 啟動開發server

```$ npm run serve```

![](https://i.imgur.com/YNVPiy5.png)


> chrome一樣有碰到localhost顯示問題(請開無痕):<br/>
>  https://localhost:8080 -> http://localhost:8080

>  或者直接編輯 package.json 指定用IP啟動

![](https://i.imgur.com/IKmpLdz.png)

 就可以開始編寫程式囉
 
####  4. 打包成上線檔案

```$ npm run build ```

> 預設會在 /dist 底下