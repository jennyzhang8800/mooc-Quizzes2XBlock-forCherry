# mooc-Quizzes2XBlock-forCherry
练习题XBlock，是为了适应http://cherry.cs.tsinghua.edu.cn/ (192.168.1.135)这台虚拟机上布署的edx平台，针对mooc-Quizzes2XBlock作了修改之后的版本。


## 部署方法

### 1. clone 代码到本地

  ` sudo git clone https://github.com/jennyzhang8800/mooc-Quizzes2XBlock-forCherry.git`
   
### 2. 安装XBlock:

先进入到mooc-Quizzes2XBlock-forCherry目录，然后安装xblock
```
cd mooc-Quizzes2XBlock-forCherry
sudo -u edxapp /edx/bin/pip.edxapp install .
```

### 3. 重启Edx服务器：

```
sudo /edx/bin/supervisorctl restart edxapp:
sudo /edx/bin/supervisorctl restart edxapp_worker:
```
## 附：

与mooc-Quizzes2XBlock相比，主要做的修改是：conf.py 中teacherGitlab的配置

## FAQ

1. 如何编辑已经发布的题目内容
2. 在编辑题目block里面载入题目进行编辑，
3. 编辑好的题目，需要在Studio对应的XBlock里面选择编辑，重新保存配置信息，最后选择右侧的发布按钮
4. 单击发布按钮以后就可以在LMS页面看到更改了
5. 注意，如果需要改变xblock的题号，那么需要删除原有的XBlock，然后重新创建新的XBlock，然后再指定题号
