# issuer
一休：将 GitHub issues &amp; comments 导出，并生成 issue 书

## 运行环境

- 目前只在 Mac OSX 中测试过

## 要求

本爬虫程序要求macbook使用Node.js，选择Homebrew安装，前提是安装Homebrew及配置github的Token：

- [安装Homebrew教程](https://blog.csdn.net/Sir_Coding/article/details/77509602)

  安装，打开终端，复制粘贴，大约1分钟左右，下载完成，过程中需要输入密码，其他无需任何操作：
     
  ```
   1  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  ```

- 安装 [Node.js 10](http://yiilib.com/topic/723/Mac%E4%BD%BF%E7%94%A8Homebrew%E5%AE%89%E8%A3%85%E6%8C%87%E5%AE%9A%E7%89%88%E6%9C%ACNodejs)（其他版本未测试） `brew install node@10`
- 安装 Git,配置Token，[参考这份教程](https://blog.csdn.net/u014175572/article/details/55510825)
- 命令行操作


## 使用方式

1. 打开命令行，下载项目，并进入项目

```bash
git clone https://github.com/hexcola/issuer
cd issuer
```

2. 在项目目录下创建 `backup` 目录，并在 `backup` 目录下分别创建 `issues` 和 `comments` 目录，你的 issue 和 comment 会分别存在这两个目录。

```bash
mkdir -p backup/issues backup/comments
```

3. 找到 `config.yml` 文件，进行修改：

    - `token`: 需要在 GitHub 上配置一个
    - `owner`: 项目所属人（组织）的名字
    - `repo`: 仓库的名字
    - 其他：默认就好

4. 安装依赖，然后运行：

```bash
npm install
node ant.js
```

## 参考

- [GitHub REST API v3](https://developer.github.com/v3/)
- [octokit/rest.js](https://octokit.github.io/rest.js/#usage)
