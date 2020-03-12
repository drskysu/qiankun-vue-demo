# 前端微服务 qiankun  demo
### demo线上地址 账号密码 admin admin
[demo地址](https://zht-test.zhonghuilv.net)
### qiankun文档
[qiankun](https://qiankun.umijs.org/zh/)

### 目录下portal为 主项目 sub-app 分别为子应用
***************
```
  动态路由项目 如需增加 子应用 tab
  在主项目 src/store/modules/user.js 中 的 getUserInfo action中配置
  在 主项目 根目录中 appInfos.js 配置 子应用 url name entry信息
```

### 解决问题
```
1: 子应用切换之间的菊花loading
2: 子应用未部署 404 提示
3: 主子应用 方法 数据传递
4: 子应用重连机制
5: 子应用共用 401 404 等页面
6: 子应用调用 主应用方法 比如 登录 授权 等
```

### 未解决
```
1: 主子应用之间 css 污染 (目前主应用采用prefixCls 避免)
2: 第一次进入 会闪烁一下
3: 子应用之间通信 （等待 2.0)
其它问题待发现..
```
### 添加 子应用项目
```
  在主应用中 src/store/modules/user.js 添加 子应用路由信息
  创建子应用
  vue create 项目名
  vue add vue-cli-plugin-chensj
```
[子应用注入插件](https://www.npmjs.com/package/vue-cli-plugin-chensj)
`其中公用组件还没编写`
### demo测试
```
  npm install
  npm run install:all
  npm run start:all
```
#### 部署服务器
```
请自行更换主应用中的 appInfos.js 文件
和子应用中 vue.config.js publicPath
```
