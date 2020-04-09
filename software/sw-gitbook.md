# gitbook-env

## 软件环境说明
- git/gitbash
- Vscode
- Github
### 一、纯Windows10环境搭建
1. 安装Git，官网下载安装，注意要勾选添加到环境变量
2. 安装Vscode，官网下载安装，插件按个人喜欢安装即可
3. 安装nodejs，官网下载安装，组件全部先择，npm必选
4. powershell以管理员权限运行，运行一下命令：`npm install gitbook-cli -g`，下载和环境准备
5. 完成后，执行：`gitbook init`，这一步才是安装，完成后既可以开始使用gitbook

### 二、Windosw10 + wsl2
1. 安装wsl2，这里选择centos(￥14),Ubuntu也一样。
2. wsl2环境初始化
   - 更新git到2.X
   - 安装nodejs，`yum install nodejs -y`
   - 部署gitbook，`npm install gitbook-cli -g`
   - 安装gitbook，`gitbook init`
   - 安装gh-pages，`npm install gh-pages -g`
3. Windows10安装Vscode，Vscode官网下载安装，插件按个人喜欢安装即可

#### 说明：以上步骤都是标准流程，经过个人实践均成功，如遇到报错请按照错误信息进行合理排错即可，npm install因网络原因可能会很慢或者报错，多次执行指令知道成功即可。

### 三、实现第一个GitHub page
1. 登录GitHub创建一个Public仓库，完成初始化后，将仓库克隆到本地，此仓库就作为Book的本地开发仓库。
2. 进入到仓库根目录，`gitbook init` ，对当前目录进行初始化(主要是为生成默认的README.md和SUMMARY.md两个文件)。
3. 对文件进行编辑，当确认内容后，`gitbook build`，会生成_book文件夹，其中就是book需要的所有文件。
4. `gh-pages -d _book`，利用gh-pages这个工具一键进行部署，同时会在远程仓库中自动创建gh-pages这个分支
5. ``，将本地的文件推送到远程仓库上
6. 在这个仓库主页中，setting-->Github Pages-->Source-->master branch /docs folder，完成后会生成一个url，这就是你的GitHub Pages.



