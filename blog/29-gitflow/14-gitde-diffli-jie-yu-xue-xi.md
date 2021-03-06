#  ❖ Git的diff理解与学习 [DRAFT]

> `git diff`和系统的`diff`命令是不同的，`git diff`是用作对比两个文件的差别，但是它是对这个文件和它在时光轴上的某个点上的自己做对比。当然`git diff`也可以用作--------

明白这点，就好理解多了。
先看这幅图：
![image](https://user-images.githubusercontent.com/14041622/36060761-9f2ead34-0e8a-11e8-857c-2ade28a723af.png)

`git diff`可以用当前工作区的某文件，来进行：@1 它和自己保存在缓冲区的复制品对比，@2 它和过去每一个commit时光点上的自己对比。
当然，对比开始后，显示结果就和系统`diff`显示的大同小异了。
```shell
# 当前工作区与缓冲区的对比
git diff [指定对比的文件，或不指定也行]

#  缓冲区与过去commits对比
git diff --staged [指定对比的文件，或不指定也行]
```

## 本次commit与上次commit的diff
[参考文章。](https://stackoverflow.com/questions/9903541/finding-diff-between-current-and-last-versions)
最简单写法：
```python
git diff HEAD^ HEAD
# or
git diff @~..@
# or
git show
# or with GUI display
git difftool HEAD^ HEAD
```

