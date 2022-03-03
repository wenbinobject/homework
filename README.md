# How to connect the test environment locally

### 1. 项目文件夹相关修改

```


├── server           服务端文件夹
│   └── config.ts    服务配置相关


// config.ts 文件夹里修改
export const NEED_PROXY = true; //使用代理改为ture
export const TARGET = 'http://api2.fbu-dev-4.bybit.com'; //你需要测试的测试服务器地址


├── env                  环境变量定义
│   └── .env.localhost   本地环境变量


// .env.localhost 文件夹里面修改

NEXT_PUBLIC_BYBIT_UNIFRAME_URL = "//www.fbu-dev-4.bybit.com" //你需要测试的测试服务器地址
NEXT_PUBLIC_BYBIT_COOKIE_DOMAIN = b_t_c_k_fbu-dev-4 //你需要测试的测试服务器地址

```

### 2. 修改系统 hosts 文件

在文件中添加

```
 127.0.0.1 local.fbu-dev-4.bybit.com //你需要测试的测试服务器地址

```

### 3. 浏览器url （localhost 替换为 local.fbu-dev-4.bybit.com） //你需要测试的测试服务器地址

```
demo
http://localhost:8000/future-activity/vip => http://local.fbu-dev-4.bybit.com:8000/future-activity/vip

```
