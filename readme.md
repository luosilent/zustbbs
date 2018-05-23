# zust校园论坛
<p>模仿laravel-china系列教程做的项目</p>
## 功能如下
用户认证 —— 注册、登录、退出；
个人中心 —— 用户个人中心，编辑资料；
用户授权 —— 作者才能删除自己的内容；
上传图片 —— 修改头像和编辑话题时候上传图片；
表单验证 —— 使用表单验证类；
文章发布时自动 Slug 翻译，支持使用队列方式以提高响应；
站点『活跃用户』计算，一小时计算一次；
多角色权限管理 —— 允许站长，管理员权限的存在；
后台管理 —— 后台数据模型管理；
邮件通知 —— 发送新回复邮件通知，队列发送邮件；
站内通知 —— 话题有新回复；
自定义 Artisan 命令行 —— 自定义活跃用户计算命令；
自定义 Trait —— 活跃用户的业务逻辑实现；
自定义中间件 —— 记录用户的最后登录时间；
XSS 安全防御；

## 克隆源代码
### 克隆 larabbs 源代码到本地：

<pre><code>git clone git@github.com:luosilent/zustbbs.git</code></pre>
 配置本地的 Homestead 环境
 运行以下命令编辑 Homestead.yaml 文件：

### homestead edit
加入对应修改，如下所示：

<pre><code>
folders:
    - map: ~/my-path/zustbbs/ # 你本地的项目目录地址
      to: /home/vagrant/zustbbs

sites:
    - map: zustbbs.test
      to: /home/vagrant/zustbbs/public

databases:
    - zustbbs
</code></pre>
### 应用修改

修改完成后保存，然后执行以下命令应用配置信息修改：

homestead provision
随后请运行 homestead reload 进行重启。

### 安装扩展包依赖
composer install
### 生成配置文件
cp .env.example .env
你可以根据情况修改 .env 文件里的内容，如数据库连接、缓存、邮件设置等。

### 生成秘钥
php artisan key:generate
### 生成数据表及生成测试数据
在 Homestead 的网站根目录下运行以下命令

$ php artisan migrate --seed
初始的用户角色权限已使用数据迁移生成。

### 配置 hosts 文件
echo "192.168.10.10   zustbbs.test" | sudo tee -a /etc/hosts
前端框架安装
1). 安装 node.js

直接去官网 https://nodejs.org/en/ 下载安装最新版本。

2). 安装 Yarn

请按照最新版本的 Yarn —— http://yarnpkg.cn/zh-Hans/docs/install

3). 安装 Laravel Mix

yarn install
4). 编译前端内容

// 运行所有 Mix 任务...
npm run dev

// 运行所有 Mix 任务并缩小输出..
npm run production
5). 监控修改并自动编译

npm run watch

// 在某些环境中，当文件更改时，Webpack 不会更新。如果系统出现这种情况，请考虑使用 watch-poll 命令：
npm run watch-poll
