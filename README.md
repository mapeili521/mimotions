# 小米运动自动刷步数

> 小米运动自动刷步数

## Github Actions 部署指南

### 一、Fork 此仓库

### 二、设置账号密码

添加名为 **USER**、**PWD**、**STEP** 的变量，值分别为 **账号（仅支持手机号）**、**密码**、**步数（0则为18000-25000之间随机 或自定义随机范围[18000-25000]）**

> Settings-->Secrets-->New secret

### 三、多账户(用不上请忽略)

多账户请用 **#** 分割 然后保存到变量 **USER** 和 **PWD**

#### 例如

**13800138000#13800138001** 变量 **USER**

**abc123qwe#abcqwe2** 变量 **PWD**

### 四、自定义启动时间

编辑 **.github/workflows/run.yml**

找到 cron: 0 10 * * *

修改其中的10为你需要修改的时间

需要运行的时间-8就是UTC时间，比如上午9点，9-8=1，则cron: 0 1 * * *

### 五、启动

> Actions-->点击“I understand my workflows, go ahead and enable them”-->All workflows-->刷步数-->点击“Enable workflow”

## 注意事项

1. 每天运行一次，在下午 6 点

2. 多账户的数量和密码请一定要对上 不然无法使用!!!

3. 启动时间得是UTC时间!

4. 如果支付宝没有更新步数,到小米运动->设置->账号->注销账号->清空数据,然后重新登录,重新绑定第三方

5.1
