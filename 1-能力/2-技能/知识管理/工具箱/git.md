# 本地分支互不干扰的开发
切换分支之前要保证当前分支修改过的文件都进行了**处理**（[commit](https://so.csdn.net/so/search?q=commit&spm=1001.2101.3001.7020)操作、stash操作），否则当前分支中没有进行处理的文件会被带到切换后的分支上，导致无法实现**分支之间互不干扰进行开发**。
