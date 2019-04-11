## 本地创建git仓库并push到github

```
// 创建本地仓库
git init
// 本地仓库关联远程仓库
git add origin https://github.com/xxx/xxx.git
git remote add  origin https://github.com/xxx/xxx.git
git push --set-upstream origin master
```