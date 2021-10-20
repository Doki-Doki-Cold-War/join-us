以下教程都将假设您使用的是主流版本的 Windows 系统。如果您使用的是 Linux，您大概率并不需要阅读这些教程，或者能自己解决遇到的问题。教程没有覆盖的问题，或其他疑问可以直接在群里询问 🍉 @suikabreaker。
## 准备步骤
1. 注册、登录 GitHub（也就是这个网站） 账户；
2. 加入这个 organization（这样你才有权限查看和修改项目）:
    1. 把你的 GitHub ID 告诉 🍉 @suikabreaker；
    2. 你会在这个网站的右上角铃铛上看到小红点，点进去并确认。
3. 从[这里](https://desktop.github.com/)下载（点击最显眼的那个紫色按钮）并安装 git 的客户端 GitHub Desktop ；
4. 从[这里](https://www.renpy.org/latest.html)下载（点击最显眼的那个绿色按钮）并安装 Ren'Py 的 SDK 和 Atom 编辑器：
    1. 按提示点击 `Extract` 后，会在你指定的位置安装，如果要改变位置可以点击 `...` 按钮；
    2. 安装完成后在那个位置打开文件夹，其中有 `renpy.exe` 和 `renpy-32.exe` 两个文件（在你的电脑上可能显示为 `renpy`、`renpy-32`），如果第一个不能打开就打开第二个；
    3. 打开界面后选择 `setting`，在 `language` 列表中找到 `Simplified Chinese` 并点击，把界面语言和开发游戏语言改为简体中文；
    4. 把工程目录设置到你觉得合适的位置，这个位置将安置我们的项目文件（点击工程目录下的蓝色字样），或者跳过这步；
    5. 点击 `文本编辑器` 下方的蓝色字样，选择 Atom 并等待下载安装完成。如果下不动（可能是未配置全局代理），可以从[这里](https://atom.io/)下载；
    6. 点击返回。
7. 克隆我们正在进行开发的仓库：
    1. 打开 Github Desktop 并登陆。如果登录不成功可能是因为你没有开启全局代理。如果你知道这是什么意思，可以尝试这条命令：`git config --global http.proxy http://<proxy-ip>:<proxy-port>`；
    2. 克隆仓库：
        1. 选择 Github Desktop 的 File->Clone reposit：
            - 在其中找到 Project X（你可以在上面的搜索框输入名称），或者
            - 点选 URL，键入 `https://github.com/Doki-Doki-Cold-War/Project-X.git`
        2. 在 Local Path 中选择之前选定的“工程目录”；
        3. 然后点击 Clone；
8. 在 Ren'Py 的 launcher 中点击刷新（工程右边），即可看到拉取下来的项目。


项目将使用 git 进行管理。如果您不清楚如何使用 git，以下是参与这个项目最起码需要了解的知识。
## Git 基本常识

待续
