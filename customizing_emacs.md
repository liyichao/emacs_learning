
所有按键都触发一个 command，command 是 Emacs 里一种特殊函数，特殊在于它是交互性的。

	(global-set-key keysequence command)

用 String 标识按键
	
	"xyz" // 按键 xyz
	"\\" // \
	"\M-?" // meta + ?
	"\C-\M-?" // ctrl + meta + ?


`apropos` command。搜索变量和函数。