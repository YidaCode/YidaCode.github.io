---
title: hexo博客多设备云同步管理
date: 2021-02-06 10:16:14
tags: [技术笔记]
---

# hexo博客多设备云同步管理
## 为什么hexo本身没办法多设备同步
首先，需要了解hexo是生成静态网页上传到github上面。<br>
因此是没有源文件的，所以没办法直接git clone下来进行多设备同步。<br>
（因为git clone下来的是hexo根据markdown生成的一些静态网页）<br>
## 那怎么办？
解决思路：在这个项目中新建一个branch专门用于存放源文件，master分支由hexo管理，<br>
而新的branch可以由多设备进行同步。<br>
具体方法：<br>
1. 先新建一个文件夹，git clone当前的blog -主要是为了拿到.git文件
2. 删除其他文件，只留下.git文件。
3. 新建一个分支hexo。git add --all||git commit n||git push origin hexo||测试一下看看是不是空文件。
4. 测试成功之后把.git转到博客的源目录下，删除theme下的git等。
5. 重新git add --all||git commit n||git push origin hexo。
6. 大功告成。
## 一些坑
1. mac需要git clone对应的hexo分支，默认还是master。
2. 直接在clone下的文件进行hexo操作会有问题，根据提示uninstall install就好了。
3. 为什么不直接在博客的源目录下直接建分支？
> 因为直接建分支会引发一些乱七八糟的冲突（试图理解过但是失败了）

- 完结散花，这篇是mac写的。