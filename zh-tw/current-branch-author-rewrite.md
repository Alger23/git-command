搜尋並修改目前分支的 commit 的作者名稱，產生新的 commit-tree

```git-bash on windows
git filter-branch --commit-filter \
'if [ "$GIT_AUTHOR_NAME" = "Author Name" ]; then \
export GIT_AUTHOR_NAME="New Author Name";\
export GIT_AUTHOR_EMAIL=new_mail@com;\
export GIT_COMMITTER_NAME="New Author Name";\
export GIT_COMMITTER_EMAIL=new_mail@com;\
fi;\
git commit-tree "$@"'
```
