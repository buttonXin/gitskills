# gitskills
- 在本地创建代码仓库后就不需要用通过clone了
  - 在本地（通过git init）创建代码仓库后就不需要用通过clone了
1. git bash 进入指令里面，然后cd到NewWeather目录下（这个NewWeather的自己离线已经写有的项目） git init  （意是将这个目录改成代码仓库），
2. git add . （添加该目录所有的内容），
3. git commit - m ‘这个随便写意思是每次提交的记录‘        这样就算提交成功了，但是没有提交到github上呢！
4. 通过进入自己的github网站，建立项目--在github 上新创建一个项目test，后面有显示Clone or   download  ，然后点击copy------> https.. .git  
5. git bash   --cd 到NewWeather 项目目录下执行
6. git remote add origin https...........git        （origin 给项目起的名字！）（https....git 就是项目地址），---没有提示就是对的！
7. 第一次init就git push -u origin master
8. git pull origin master-----在push钱先pull  ！！！按 esc  如果瑞不出了  就按 ctrl + c  然后 输入 ：wq  （强制退出保存） ：q（强制退出）
9. git push origin master       ---》master就是代码在master 分支上！）
10. 之后我的会出现username：buttonXin
11. 然后弹出了一个输入密码：****
12. 如果没有显示100％ 的字样就表示不成功，请从第7步或者第6步开始
13.   没有提示fail 就成功了！
----------------------------------------------------------------
- 直接通过clone

1. 在github 项目上test ，复制地址 https......git  
2. cd到本项目下 （不需要进行git init 初始化！！） 直接git clone https.....git （这样就把test项目clone到本地了）
3. 然后通过as 导入该项目！，尽情的操作项目，
4. 之后 git bush 到该项目目录下--git add .    （添加所有修改的，也可以git Xxx.java--需要进入Xxx.java目录下）
5.   git commit -m ‘内容标签’（执行提交就行了）
6. 最后执行 git push origin master （这样就把本地代码提交到github上去了）
7. 然后去github哩就可以看到自己提交的记录..和修改的记录，与最终的代码

------------------------------------------------------------------------------

- 廖雪峰的git  learn 记录
  - 当每天完成一次修改的时候， 就cd 进入目录 然后
* 提交git到github
    * git add .  
    * git commit -m ‘添加更改的信息’
    * git push origin master 
* 通过log ，返回到上一版本
    * git log 查看所有版本信息
    * git reset --hard HEAD~   （2个  -- ！！后面的~代表的是第一个最新的版本，可以用 ~20  代表从最新版本到20版本之后的版本）
    * 之后再次打开本项目，就到了~代表的项目中了！
    * 如果关闭了git bash  重新回到本项目中，输入git reflog  （reflog！！） 可以看到每一版本前面的commit  id  
    * 输入git reset --hard  1485c36f   就回到了   1485c36f   对应的版本中去了！
*  撤销修改
    * 当项目修改后，没有add 但是修改的还多，所以需要用git checkout -- file   （file是文件的目录路径名比如：
app/src/main/java/com/demo/newweather/activity/TestActivity.java
）
* 删除文件
    * 先添加一个文件，然后git 并且提交后，想删除，通过外面文件管理器删除，
    * 但是git status里面会显示出那个文件被删除了，这时有2中选择
    * 1.确定想删除 git rm  file    （
file---->>> app/src/main/java/com/demo/newweather/activity/TestActivity.java代表删除的路径名里面的文件
）然后 git commit -m “确定提交”就不报错了
    * 2.是删错了，想恢复过来，git checkout -- file   (  ../  ../ ..  ) 就可以一键还原了！
* 从远程库克隆
    * 1.  首先如果克隆别人的项目，先cd到一个空的文件夹下，然后git clone 网址   等待clone完毕 就可以了
    * 2.  （怎么在自己已经写的项目中从远程clone？？）
* 创建分支
    * git checkout -b dev   （相当于这2个操作git branch dev   git checkout dev）意思是创建dev分支并切换到dev的分支上
    * git branch 查看当前分支 前面带有*号的就是
    * 然后再dev 分支上 git add file     git commit -m “内容”这是master上并没有该add的内容
    * git checkout master  切换到主master分支上
    * git merge  dev   表示将分支dev中add  commit 内容合并到master上！
    * git branch -d dev  表示安心的删除dev分支了
---------------

AS上的使用
   > as上创建项目后可以直接使用VCS里的import into Version Code ，选择Share Project to GitHub 就直接在GitHub创建项目了
   > 然后在选择Create Git Repository ，选择这个项目的根目录，进行创建，这样就将本地与GitHub进行关联了
