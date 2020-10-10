mock.js系列 學習筆記
===

###### tags: `技術`

## 資源

[github-axios-mock-adapter](https://github.com/ctimmerm/axios-mock-adapter)
[Summer-Vue.js: axios 與 axios-mock-adapter](https://cythilya.github.io/2017/11/02/vue-axios/)

## 其他的mock

[github-Mock](https://github.com/nuysoft/Mock)
[mockjs 官網文件](http://mockjs.com/examples.html)
[github-better-mock](https://github.com/lavyun/better-mock)
[Better-Mock 官網](https://lavyun.github.io/better-mock/)

[掘金-使用Mock.js模拟数据请求](https://juejin.im/post/6844903571381551111)
[Medium-使用 Mock 自己產生假資料](https://medium.com/@happyjayxin/%E4%BD%BF%E7%94%A8-mock-%E8%87%AA%E5%B7%B1%E7%94%A2%E7%94%9F%E5%81%87%E8%B3%87%E6%96%99-fc939acfeae2)


## 名詞

axios-mock-adapter: 給axios.js使用的Mock工具
Mock: 拿來攔截Ajax，產生模擬數據 // 已停止維護
better-mock: 其他人接手後，可以相容原Mock.js的新工具

> 讓前端可以自行產生假的後端回應

### 優點

* 不用等後端API完整開發完成才串接
* 不用改寫原本的Ajax方法
* 可以模擬正常狀況難以觸發的後端回應

---

## 機制


1. 安裝

```npm install axios-mock-adapter --save-dev```

2. 使用

* 在src底下新增 mock資料夾，用來存放相關檔案 & 在main.js引用
* 或者直接在打API的方法裡使用


