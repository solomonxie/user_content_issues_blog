# Vim鼠标支持问题

Vim高版本默认是支持鼠标滚动的。但是在Tmux中就不可以。

这样可以通过在`~/.vimrc`中设置`set mouse=a`来达到开启鼠标支持的左右。
`a`模式为`all`，即鼠标的"完全支持模式": 在所有情况下都支持鼠标，包括鼠标定位到某行，定位到某个单词，双击选择单词，三击选择整行，甚至在tmux中也一样。

但是`set mouse=a`有一个缺点不好解决就是：鼠标选择文字的话，会默认进入Visual模式。
