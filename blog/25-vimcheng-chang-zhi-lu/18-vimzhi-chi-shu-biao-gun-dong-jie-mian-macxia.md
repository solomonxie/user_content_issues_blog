# Vim支持鼠标滚动界面
Mac下，Vim支持鼠标滚动光标，通过光标移动上下翻动页面。但是这样太别扭了，我们需要的是滚轮控制界面滚动，如vim中`ctrl+e`一样的效果。
简单：`~/.vimrc`中加一句`set mouse=a`即可。
不过这样设置会导致每次用鼠标选择一段文本都会自动进入visual模式，这样的话我们就没法复制到系统剪切板了。
网上说mouse后一个-好即可，如`set mouse-=a`，但是试过没用。
这时候，需要按住`Alt`键然后再用鼠标选择文本，这样一来就不会启动v模式，且可以复制到剪切板。
