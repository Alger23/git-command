刪除分支
=======

刪除本地分支
-----------

```bash
git branch -d <branch_name>
```

或是

```bash
git branch -D <branch_name>
```

### 參數說明
* -d ：--delete 只能刪除已合併(merged)的分支
* -D ：--delete --force 強制刪除分支


刪除遠端分支
-----------

[Git v1.7.0](https://github.com/gitster/git/blob/master/Documentation/RelNotes/1.7.0.txt)
```bash
git push origin --delete <branch_name>
```


[Git v1.5.0](https://github.com/gitster/git/blob/master/Documentation/RelNotes/1.5.0.txt)
```bash
git push origin :<branch_name>
```

### 然後需要在其它終端接收異動

```bash
git fetch --all --prune
```
