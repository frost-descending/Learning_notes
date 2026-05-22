# 将windows下的代码上传到GitHub 或者 Gitee

## 1.生成密钥
> ssh-keygen -t ed25519 -C "your_email@example.com"
> 
> 获取密钥:
> type %userprofile%\.ssh\id_ed25519.pub
>
## 2.把公钥绑定到 Gitee 网页端
>1.  打开浏览器，登录你的 Gitee (码云) 账号。

>2.  点击网页右上角你的个人头像，在弹出的菜单中选择 设置（Settings）。

>3.  在左侧的导航菜单栏中，找到 安全设置 分组，点击里面的 SSH公钥。

>4.  填写右侧的表单：
    标题： 随便起个名字，比如 Windows_CMD_Gitee。
    公钥： 将你刚刚在 CMD 中复制的那段长字符串，完整粘贴到这个大文本框中。

>点击下方的 确定 按钮，系统会提示你输入 Gitee 账号密码进行安全验证，验证通过后即绑定成功。


## 3.在 CMD 中激活并验证连接（最关键的一步）

>ssh -T git@gitee.com

>⚠️ 极其重要的交互提示：

因为这是你的电脑第一次通过 SSH 连接 Gitee，CMD 屏幕上一定会弹出一行警告：
Are you sure you want to continue connecting (yes/no/[fingerprint])?

正确操作： 此时千万不要直接敲回车！你必须在光标处手动输入小写的 yes 三个字母，然后按下 回车键。

成功标志： 随后屏幕上会输出：
Hi XXX! You've successfully authenticated, but GITEE.COM does not provide shell access.
（只要看到 successfully authenticated 和你的 Gitee 用户名，就说明 Gitee 的 SSH 密钥已经彻底配好并激活了！)

### 4.git
>密钥激活后，你就可以直接去 Gitee 建个空白仓库（不要勾选初始化 README），复制它的 SSH 地址，然后进到你的新项目文件夹的 CMD 窗口里，运行你刚才学到的命令：

`cd C:\path\to\your\new_project`
`git init`
`git commit -m "first commit"`
`git branch -M main`
`git remote add origin git@gitee.com:your_username/your_repository.git`
`git push -u origin main`