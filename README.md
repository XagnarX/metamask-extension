# MetaMask Browser Extension

## fork细节
```shell
commit 9f95f30cea54d2711798f673614ffb2e54cc071c (HEAD -> develop, origin/develop, origin/HEAD)
Author: Charly Chevalier <charly.chevalier@consensys.net>
Date:   Fri Jul 12 22:52:59 2024 +0200

```

## 修改细节
- 隐藏私钥
![隐藏私钥](https://raw.githubusercontent.com/songyaoshun/cloudimgs/main/images/%E9%9A%90%E8%97%8F%E7%A7%81%E9%92%A5.jpg)

- 隐藏私钥助记词
![隐藏私钥助记词](https://raw.githubusercontent.com/songyaoshun/cloudimgs/main/images/%E9%9A%90%E8%97%8F%E7%A7%81%E9%92%A5%E5%8A%A9%E8%AE%B0%E8%AF%8D.jpg)

## 本地build
使用的电脑macos，步骤：

1. 安装 Node.js 版本 20：

    ```shell
    nvm install 20
    nvm use 20
    ```

2.	启用 Corepack 并安装4.2.2版本的yarn：
    ```shell
    corepack enable
    corepack prepare yarn@4.2.2 --activate

    yarn --version
    ```

3.	复制并重命名配置文件：
    ```shell
    cp .metamaskrc{.dist,}
    ```

4.	配置 .metamaskrc 文件：
  - 替换 INFURA_PROJECT_ID 为你的 Infura API Key。
  - 可选：添加 SEGMENT_WRITE_KEY 和 SENTRY_DSN。

5.	安装依赖：
    ```shell
    yarn install
    ```
6.	构建项目：
    ```shell
    yarn dist

    # 构建之后压缩包路径
    open builds
    ```

按照以下说明验证本地构建是否正确运行：

  - [如何将自定义构建添加到 Chrome](./docs/add-to-chrome.md)
  - [如何将自定义构建添加到 Firefox](./docs/add-to-firefox.md)


补充：
第4步的key请在 https://app.infura.io/ 申请。
大致效果：
![202407131551621](https://raw.githubusercontent.com/songyaoshun/cloudimgs/main/images/202407131551621.png)

替换后的大致效果：
![202407131553450](https://raw.githubusercontent.com/songyaoshun/cloudimgs/main/images/202407131553450.png)