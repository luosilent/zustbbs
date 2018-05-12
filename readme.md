# laravel+bbs论坛项目

## 功能如下

### 分三部分

<ol><li>角色</li>
<li>信息</li>
<li>动作</li>
</ol>

<h3>1. 角色</h3>
<p>在我们的 LaraBBS 里，将会出现以下角色：</p>
<ul><li>游客 —— 没有登录的用户；</li>
<li>用户 —— 注册用户，没有多余权限；</li>
<li>管理员 —— 辅助超级管理员做社区内容管理；</li>
<li>站长 —— 权限最高的用户角色。</li>
</ul>

<p>角色的权限从低到高，高权限的用户将包含权限低的用户权限。</p>
<h3>2. 信息结构</h3>
<p>主要信息有：</p>
<ul><li>用户 —— 模型名称 User，论坛为 UGC 产品，所有内容都围绕用户来进行；</li>
<li>话题 —— 模型名称 Topic，LaraBBS 论坛应用的最核心数据，有时我们称为帖子；</li>
<li>分类 —— 模型名称 Category，话题的分类，每一个话题必须对应一个分类，分类由管理员创建；</li>
<li>回复 —— 模型名称 Reply，针对某个话题的讨论，一个话题下可以有多个回复。</li>
</ul>

<h3>3. 动作</h3>
<p>角色和信息之间的互动称之为『动作』，动作主要由以下几个：</p>
<ul><li>创建 Create</li>
<li>查看 Read</li>
<li>编辑 Update</li>
<li>删除 Delete</li>
</ul>


<h2>用例</h2>

<h3>1. 游客</h3>
<ul><li>游客可以查看所有话题列表；</li>
<li>游客可以查看某个分类下的所有话题列表；</li>
<li>游客可以按照发布时间和最后回复时间进行话题列表排序；</li>
<li>游客可以查看单个话题内容；</li>
<li>游客可以查看话题的所有回复；</li>
<li>游客可以通过注册按钮创建用户（用户注册，游客专属）；</li>
<li>游客可以查看用户的个人页面；</li>
</ul>

<h3>2. 用户</h3>
<ul><li>用户可以在某个分类下发布话题；</li>
<li>用户可以编辑自己发布的话题；</li>
<li>用户可以删除自己发布的话题；</li>
<li>用户可以回复所有话题；</li>
<li>用户可以删除自己的回复；</li>
<li>用户可以编辑自己的个人资料；</li>
<li>用户可以接收话题新回复的通知。</li>
</ul>

<h3>3. 管理员</h3>
<ul><li>管理员可以访问后台；</li>
<li>管理员可以编辑所有的话题；</li>
<li>管理员可以删除所有的回复；</li>
<li>管理员可以编辑分类；</li>
</ul>

<h3>4. 站长</h3>
<ul><li>站长可以编辑用户；</li>
<li>站长可以删除用户；</li>
<li>站长可以修改站点设置；</li>
<li>站长可以删除分类；</li>
</ul>