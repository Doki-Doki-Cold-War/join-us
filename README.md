## 准备步骤

以下教程都将假设您使用的是主流版本的 Windows 系统。如果您使用的是 Linux，您大概率并不需要阅读这些教程，或者能自己解决遇到的问题。教程没有覆盖的问题，或其他疑问可以直接在群里询问 🍉 @suikabreaker。

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
    1. 打开 Github Desktop 并登陆。如果登录不成功可能是因为你没有开启全局代理。如果你知道这是什么意思，可以尝试这条命令：`git config --global https.proxy https://<proxy-ip>:<proxy-port>`；
    2. 克隆仓库：
        1. 选择 Github Desktop 的 File->Clone reposit：
            - 在其中找到 Project X（你可以在上面的搜索框输入名称），或者
            - 点选 URL，键入 `https://github.com/Doki-Doki-Cold-War/Project-X.git`
        2. 在 Local Path 中选择之前选定的“工程目录”；
        3. 然后点击 Clone；
8. 在 Ren'Py 的 launcher 中点击“刷新”（工程右边），即可看到拉取下来的项目。

现在，在 Ren'Py 的 launcher 中选择项目“Project X”，点击“启动项目”，如果一切正常，你将看到最新版本的游戏。

## Git 基本常识

项目将使用 git 进行管理。如果您不清楚什么是 git 以及如何使用，以下是参与这个项目最起码需要了解的知识。

### 文件同步

我们的项目**托管**在了 GitHub 上，它起到的最基本的作用可以理解为文件同步，保管我们的工作成果，并在所有参与项目的成员间**共享进度**。

任何新成员加入或者要在新设备上重新准备开发环境时，通过前面“准备步骤”的流程，都可以把之前积累了我们劳动的项目从 GitHub 完整地获取。

在之后的开发过程中，每次开始工作前都可以先“拉取”(pull) git 库最新的改动，把我们本地保存的项目同步到最新；在完成我们的工作后并“提交”（commit）后，“推送”（push）到 GitHub 上，让大家能拉取你刚刚完成的改动。

**要拉取**，在 GitHub Desktop 上点击 `Repository`->`Pull`，或者使用快捷键 Ctrl+Shift+P。

**要上传改动**，在 GitHub Desktop 界面上 Changes 栏下勾选想要修改的文件（注意，如果不勾选，这个修改将只在你的设备上存在），在你的头像边的输入框输入你这次改动的说明（**务必让你的说明能反映这次改动的意义**），然后点击下方的“commit to main”**提交**改动，再点击 `Repository`->`Push`，或者使用快捷键 Ctrl+P，来把提交的改动**推送**，同步到 GitHub。

注意：如果你没有推送，你的修改将只保存到你本地的 git 仓库。如果你在提交前做了好几个不同意义的工作，可以在每件工作后进行一次“提交”，最后再一次性“推送”给 GitHub。

### 进阶

Git 是一种**版本管理**系统。我们所有修改的历史都有记录，随时可以倒退到之前任何一个历史版本，然后再切换回来。这意味着，版本管理能给你**安全感**。你可以不必担心自己提交了什么破坏性的内容，删除、覆盖、修改的文件，都可以通过回退版本找回来。

每个提交（commit），其实就是历史里的一个节点。

而且，Git 的“历史”是可以有分支的。这意味着**我们可以互不干扰地协作**：我和你同时修改项目，我修改了界面的 UI，你添加了一段新的剧情，并都提交到了 GitHub。现在有了两个不同的版本，这时 Git 的历史产生了分叉。后一个提交的人会发现自己的提交已经和历史主线脱离了，这时 git 可以自动“合并”（merge）分支，把两条历史支线合并在一起，魔法般地，两个人提交的改动就都生效了——我们现在的历史主线版本既有新的 UI 又有新的剧情。

注意：如果发生了这种情况，你需要在正常的“上传改动”操作中，推送前再加上拉取的操作。有一定可能，两人同时修改了同一文件的同一部分，这时需要手动合并分支。如果你对自己有信心可以尝试根据软件的提示进行，或者直接找 🍉 @suikabreaker。

而且，Git 的历史其实同时存在于你的电脑和 GitHub 上。你可能保存了一些 GitHub 没有的节点，GitHub 也可能保存你没有的节点，当你推送（push）时，就把一条历史路径上 GitHub 没有的节点发送给了 GitHub。你拉取（pull）时，就获取了这条历史路径上你缺少的节点。

Git 是基于“差异”（diff）管理版本的，它会记录两个节点之间的差异，而不是记录完整的新节点。这意味着 git 可以进行一些魔幻操作：A->B->C 的历史路径中，我可以独立于 B，把 B->C 的修改应用在 A 上，产生一条只发生了 A 和 C，没有发生 B 的新历史。在实际应用中，如果我们连续修改了两次剧情，但是对第一次的修改不满意，可以在不放弃第二次修改的前提下撤回第一次修改。

Git 能做到的事情还有更多，我们可以同时维护多个版本分支（branch），可以检索历史，追溯每个改动是谁提交的。

这些复杂操作如果你搞不定，随时找 🍉 @suikabreaker。
