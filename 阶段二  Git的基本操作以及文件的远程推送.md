**阶段二  Git的基本操作以及文件的远程推送**

*一、Git的基本操作*

1、Git的文件操作

1）文件的4种状态

Untracked:未跟踪。通过**git add** 状态变为**staged**。

Unmodify:文件已入库，未修改。如果它被修改，则变为**Modified**。如果使用**git rm**移出版仓库，则成为**Untracked**文件。

Modified:文件已修改，仅仅只是修改，未进行其它操作。

Staged:暂存状态。执行**git commit**，则将修改同步到库中，这时库中的文件与本地文件又变得一致，文件为**Unmodify**状态。执行**git reset HEAD filename** 取消暂存，文件状态为**Modified**。

2）查看文件状态

#查看指定文件状态：git status【filename】

#查看所有文件状态：git status

#git add.    添加所有文件到暂存区

#git commit -m       提交暂存区中的内容到本地仓库

3）文件的修改

第一次修改 -> `git add` -> 第二次修改 -> `git add` -> `git commit`

2、版本回退

首先，Git必须知道当前版本是哪个版本，在Git中，用`HEAD`表示当前版本。然后，我们要把当前版本`append GPL`回退到上一个版本`add distributed`，就可以使用`git reset`命令。Git的版本回退速度非常快，因为Git在内部有个指向当前版本的`HEAD`指针，当你回退版本的时候，Git仅仅是把HEAD从指向`append GPL`：

```ascii
┌────┐
│HEAD│
└────┘
   │
   └──> ○ append GPL
        │
        ○ add distributed
        │
        ○ wrote a readme file
```

改为指向`add distributed`：

```ascii
┌────┐
│HEAD│
└────┘
   │
   │    ○ append GPL
   │    │
   └──> ○ add distributed
        │
        ○ wrote a readme file
```

然后顺便把工作区的文件更新了。所以你让`HEAD`指向哪个版本号，你就把当前版本定位在哪。当你用`$ git reset --hard HEAD^`回退到`add distributed`版本时，再想恢复到`append GPL`，就必须找到`append GPL`的commit id。

*二、文件的远程推送*

1、创建SSH key（我摸索了好久，终于找到了！）

$ ssh-keygen -t rsa -C "202221091047@mail.scuec.cn"

![](C:\Users\lenovo\Desktop\QQ截图20221103112126.png)

2、添加远程库

在远程Github中建立自己的新仓库（如：我建的second Task）；获取到新仓库的地址后，输入git remote add origin ttps://github.com/zyyxxxxxxx/second-Tasks.git关联远程仓库。

3、将本地仓库push到远程仓库

git push -u origin master（如：样例所示）

![](C:\Users\lenovo\Desktop\2018042815224193.png)

4、最后在远程Github仓库中就能看到自己需要的"Hello 邹雨希.md"的文件

*三、我遇到的一些问题*

1.没有搞清楚SSH key在哪里。

2.不知道怎样将本地仓库与远程仓库关联。

3.第一次使用Git，还没有弄清它的一些功能和使用方法。



