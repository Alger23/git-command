搜尋並修改目前分支的 commit 的作者名稱，產生新的 commit-tree

```git-bash on windows
git filter-branch --commit-filter \
'if [ "$GIT_AUTHOR_NAME" = "Chen, Wen-Wei" ]; then \
export GIT_AUTHOR_NAME="Alger";\
export GIT_AUTHOR_EMAIL=alger.chen23@gmail.com;\
export GIT_COMMITTER_NAME="Alger";\
export GIT_COMMITTER_EMAIL=alger.chen23@gmail.com;\
fi;\
git commit-tree "$@"'
```
