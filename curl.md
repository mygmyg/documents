# 给 iTerm 终端设置代理
### 1.设置代理

使用 curl，wget，brew等http应用程序会调用http_proxy和https_proxy这两环境变量进行代理，通过下面方式设置：

export http_proxy=http://127.0.0.1:8087
export https_proxy=$http_proxy
### 2.取消设置

```
unset http_proxy https_proxy
```
### 3.快速切换

可以在 ~/.zshrc 或者 ~/.bash_profile 中添加这样的alias：

alias goproxy='export http_proxy=http://127.0.0.1:8087 https_proxy=http://127.0.0.1:8087'
alias disproxy='unset http_proxy https_proxy'
这样下次就可以很方便地切换proxy了！

### 参考

[curl 设置代理](http://honglu.me/2015/11/06/%E7%BB%99iTerm%E7%BB%88%E7%AB%AF%E8%AE%BE%E7%BD%AE%E4%BB%A3%E7%90%86/)