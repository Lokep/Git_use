### 2019/9/20

切换分支 ` git checkout ${分支名} `
创建分支并切换 ` git checkout -b ${分支名} ` =>
  1. ` git branch ${分支名}`
  2. ` git checkout ${分支名} `
  
但是，在创建分支时，使用错了模板，所以需要删除当前本地分支

先查看了当前的分支  ` git branch -a `

![Image text]( https://github.com/Lokep/Git_use/blob/master/img/delete-branch/aeb338c31e21f2dd5b89ef838a815dd.png)

删除本地分支的指令为 ` git branch -d ${branch-name} ` || ` git branch -D ${branch-name} ` //-D 为强制删除

但是在删除时一直提示 无法删除

![img](https://github.com/Lokep/Git_use/blob/master/img/delete-branch/91301235bc79c4fef60bfb2ae37f2ea.png)

在一波百度之后，错误原因很有可能是你正处于该分支上，然后尝试删除该分支是不被允许的。

所以先将当前分支切换到别的分支，然后再执行 ` git branch -d ${branch-name} `,

就有了如下 提示，就是在新分支存在修改

![img](https://github.com/Lokep/Git_use/blob/master/img/delete-branch/1568956874.jpg)

在执行 ` git commit -m "" `之后，执行删除指令的时候，可以看到提示

![img](https://github.com/Lokep/Git_use/blob/master/img/delete-branch/1568956954.jpg)

所以选择强制删除 ` git branch -D ${branch-name} `
![img](https://github.com/Lokep/Git_use/blob/master/img/delete-branch/9174e49407cd0ac207c8af9f865ad1b.png)
