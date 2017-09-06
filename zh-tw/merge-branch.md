合併分支
=======

```
git checkout master
git merge --squash develop
git commit
```


### 使用別人的提交合併
```
git checkout master
git merge --squash develop -S recursive -X theirs
```
