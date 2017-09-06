建立新的無內容分支
================

```bash
git checkout --orphan empty-branch
git rm -rf
git commit --allow-empty -m "root commit"
git push origin empty-branch
```
