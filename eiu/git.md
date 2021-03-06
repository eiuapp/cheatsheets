---
title: Git
category: Git
layout: 2017/sheet
---

### Check your information 

```bash
git config --global --list
```

### Delete all changes in the Git repository, but leave unstaged things 

```bash
git checkout .
```

### Delete all changes in the Git repository, including untracked files 

```bash
git clean -f
```

### git客户端连接ssh端口不是22的git仓库 ###

```bash
git clone http://192.168.168.164:5080/FED/lvchuang-web.git
git clone ssh://git@192.168.168.164:5022/FED/lvchuang-web.git
```

- https://blog.csdn.net/intergameover/article/details/50186239

### git diff old mode 100644 new mode 100755

执行git diff filename ,出现

```bash
old mode 100644 new mode 100755 的提示
```

```bash
git config --add core.filemode false
```

如果要全局设置, 则

```bash
git config --global core.filemode false
```
https://stackoverflow.com/questions/1257592/how-do-i-remove-files-saying-old-mode-100755-new-mode-100644-from-unstaged-cha
https://blog.csdn.net/ai2000ai/article/details/79628896

### Git 查询某次历史提交的修改内容 ###

我们首先

git log显示历史的提交列表：

git show <commit-hashId> 便可以显示某次提交的修改内容

同样 git show <commit-hashId> filename 可以显示某次提交的某个内容的修改信息。



### Git获取Commit修改文件列表 ###


```bash
git diff --name-only HEAD~ HEAD
git diff --name-only HEAD~3 HEAD
```

### 查看文件最近n次提交的修改 ###

```bash
git log -p -2 src/components/tabView/efficiency/CompanyAssess.vue
```

## ref
- https://github.com/arslanbilal/git-cheat-sheet
- http://bilalarslan.me/git-cheat-sheet/
- https://blog.csdn.net/intergameover/article/details/50186239
