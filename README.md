# How to connect the test environment locally

### 1. Modify the project folder

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

### 2. Modify the hosts file of the system

在文件中添加

```
 127.0.0.1 local.fbu-dev-4.bybit.com //你需要测试的测试服务器地址

```

### 3. Browser URL (localhost replaced with local.fbu-dev-4.bybit.com) // Address of the test server you need to test

```
Demo
http://localhost:8000/future-activity/vip => http://local.fbu-dev-4.bybit.com:8000/future-activity/vip

```

