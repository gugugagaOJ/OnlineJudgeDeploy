简体中文 | [English](https://github.com/gugugagaOJ/OnlineJudgeDeploy/blob/master/README.en.md)


## 环境准备

### Linux 环境

1. **安装 Docker 和 Docker Compose**

   本项目已经将所有依赖打包进 Docker 镜像，您只需要确保系统中已经安装了 Docker 和 Docker Compose 即可。

   * 安装 Docker：

     * 国内用户可以使用以下脚本一键安装 Docker：

       ```bash
       sudo curl -sSL https://get.daocloud.io/docker | sh
       ```

     * 国外用户可以使用以下脚本一键安装 Docker：

       ```bash
       sudo curl -sSL get.docker.com | sh
       ```

   * 安装 Docker Compose：

     ```bash
     sudo apt-get update && sudo apt-get install -y docker-compose
     ```

   详细的安装步骤可以参考官方文档：[Docker 安装文档](https://docs.docker.com/install/)

2. **安装 Git 和必要的工具（可选）**

   如果你的系统中还没有安装 Git 和其他常用工具，可以使用以下命令进行安装：

   ```bash
   sudo apt-get update && sudo apt-get install -y git curl vim
   ```

   这些工具并非必须，但如果你需要进行一些定制化配置或调试，它们会非常有用。



### Windows 环境


Windows 下的安装仅供体验，勿在生产环境使用。如有必要，请使用虚拟机安装 Linux 并将 OJ 安装在其中。

以下教程仅适用于 Win10 x64 下的 `PowerShell`

1. 安装 Windows 的 Docker 工具
2. 右击右下角 Docker 图标，选择 Settings 进行设置
3. 选择 `Shared Drives` 菜单，之后勾选你想安装 OJ 的盘符位置（例如勾选D盘），点击 `Apply`
4. 输入 Windows 的账号密码进行文件共享
5. 安装 `Python`、`pip`、`git`、`docker-compose`，安装方法自行搜索。

## 开始安装

1. 请选择磁盘空间富余的位置，运行下面的命令

    ```bash
    git clone https://github.com/gugugagaOJ/OnlineJudgeDeploy.git && cd OnlineJudgeDeploy
    ```

2. 启动服务

    ```bash
    docker-compose up -d
    ```


根据网速情况，大约5到30分钟就可以自动搭建完成，全程无需人工干预。

等命令执行完成，然后运行 `docker ps -a`，当看到所有的容器的状态没有 `unhealthy` 或 `Exited (x) xxx` 就代表 OJ 已经启动成功。

## 尽情享用吧

通过浏览器访问服务器的 HTTP 80 端口或者 HTTPS 443 端口，就可以开始使用了。后台管理路径为`/admin`, 安装过程中自动添加的超级管理员用户名为 `root`，密码为 `rootroot`， **请务必及时修改密码**。

不要忘记阅读文档 http://opensource.qduoj.com/

## 定制

2.0 版将一些常用设置放到了后台管理中，您可以直接登录管理后台对系统进行配置，而无需进行代码改动。

若需要对系统进行修改或二次开发，请参照各模块的**README**，修改完成后需自行构建Docker镜像并修改`docker-compose.yml`

## 遇到了问题？

请参照: [http://opensource.qduoj.com/](http://opensource.qduoj.com/#/onlinejudge/faq) ，如有其他问题请入群讨论或提issue。
