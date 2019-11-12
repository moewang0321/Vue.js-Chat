<!--
 * @Author: MoeWang
 * @Date: 2019-11-10 17:41:33
 * @LastEditors: 
 * @LastEditTime: 2019-11-12 17:57:59
 * @FilePath: \vue-chatkit\README.md
 -->
# 基于Vue的聊天室实现

使用了pusher的chatkit插件和管理，注册需要在后台由管理员添加用户，权限可由管理员在pusher/chatkit提供的后台进行操作

## 项目安装
```
npm install
```

### 编译和热加载以用于开发模式
```
npm run serve
```

### 编译和压缩以用于生产模式
```
npm run build
```


### 自定义配置和支持网站
👀 [cli-vue](https://cli.vuejs.org/config/).

👀 [@pusher/chatkit](https://pusher.com/chatkit).



## Pusher控制

### 官网

[pusher]: https://pusher.com/chatkit

在此网址按步骤配置`chatkit`

进入chatkit控制台，创建新的chatkit

![](https://i.loli.net/2019/11/12/ABKiOyC3bmMPXD5.png)

新建一个控制台的名字 **必要的**

![](https://i.loli.net/2019/11/12/WKUpeV7EQqklOwu.png)



在控制台中创建你的第一个用户，默认为admin管理员

![](https://i.loli.net/2019/11/12/CvO3oVFzHASptmT.png)



创建用户，房间以及用户权限



![](https://i.loli.net/2019/11/12/q6WlJezX4NRucMr.png)

最后在下图中找到 `Instance Locator`和` Test Token `,替换掉根目录里中`.env.local`文件中全局变量`VUE_APP_INSTANCE_LOCATOR`和`VUE_APP_TOKEN_URL` 的值











