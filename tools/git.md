## 本地创建git仓库并push到github

```
// 创建本地仓库
git init
// 本地仓库关联远程仓库
git add origin https://github.com/xxx/xxx.git
git remote add  origin https://github.com/xxx/xxx.git
git push --set-upstream origin master
```

## commit message 规范
基本格式
```
<type>(<scope>): <subject> 
<BLANK LINE> 
<body> 
<BLANK LINE> 
<footer>
```
type说明:
+ init: 项目初始化
+ feat：新功能（feature）
+ fix：修补bug
+ docs：文档（documentation）
+ opt：优化和改善，比如弹窗进行确认提示等相关的，不会改动逻辑和具体功能等
+ style： 格式（不影响代码运行的变动）
+ refactor：重构（即不是新增功能，也不是修改bug的代码变动）
+ test：增加测试
+ save：单纯地保存记录
+ other：用于难以分类的类别（不建议使用，但一些如删除不必要的文件，更新.ignore之类的可以使用）
