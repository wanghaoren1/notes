**初始化Git仓库**

​	在项目目录下右键打开 git  bash

​		git   init

**配置用户信息**

​	就是在git设置当前使用者的用户，每一次备份都会把当前备份者的信息存储起来

​	git	config	--global	user.name	"hao"

​	git	config	--global	user.email	"1326711848@qq.com"

**存储代码到.get仓储**

​	git	add	    ./1.txt     把指定的文件放到仓储大门口

​	git	add	    ./		    把所有的文件放到仓储大门口

​	git    commit    - m     "这次操作的说明"

​	git    commit  --all   -m  "这些操作的说明"       //不用放到大门口，直接放到仓库

​	git   rm     ./ 1.txt     删除指定文件，删除后要执行commit操作

**查看当前状态**

​	可以查看当前代码是否放到仓库中

​	git    status

**查看日志**

​	git    log      查看历史提交的日志

​	git    log    --oneline     查看简洁版的日志

**版本回退**

​	git    reset    --hard   Head~0      //回退到上一次提交时的状态

​	git    reset    --hard   Head~      //回退到上上一次提交时的状态

​	git    reset     --hard   [版本号]      //通过版本号精确回退

​	git    reflog                               //可以看到每一次切换版本的记录：可以查看所有提交的版本号

**分支**

​	默认有一个主分支 master

​	**创建分支**

​		创建一个分支dev，在刚创建的时候，dev和master分支里的内容是一样的

​		git     branch     dev

​	**查看分支**

​		查看当前有哪些分支

​		git       branch

​	**切换分支**

​		切换到指定的分支

​		git  checkout    dev 

​	**合并分支**

​		把指定的分支合并到当前分支，当前分支指 通过git     branch命令，查出分支前面带有  *   的分支。

​		合并时如果有冲突，需要手动去处理，处理后还要在提交一次

​		git    merge    dev

​	**提交代码到GitHub**

​		GitHub不是Git，只是一个网站，可以通过git上传代码

​		把当前分支代码上传到master分支上

​		git     push    [地址]   master

​		把远程master分支代码下载到本地

​		git   pull   [地址]    master       不会覆盖

​		git   clone  [地址]     会进行覆盖，首次获取可以

**通过SSH上传代码**

​	公钥，私钥，连着是有关联的

​	ssh-keygen  -t  rsa  -C  "1326711848@qq.com",打开用户目录，找到.ssh

​	在远程仓库设置Setting

​	输入命令 ssh -T git@github.com，输入yes

**在push和pull操作都进行时**

​	先pull，再push

**push与pull简写操作**

​	git  remote  add  origin   git@github.com:wanghaoren1/test152.git

​	git    pull   origin   master

​	git    push   origin  -u  master

​	git   pull /push    就可以了



​	