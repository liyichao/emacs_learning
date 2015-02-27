* `defun`

	
		(defun other-window-backward (&optional n)
			(interactive "P")
			(other-window (- (prefix-numeric-value n))))

* `defalias` 重命名某函数

* `Hook`。`Hook`是 Lisp 变量，其值是函数列表，这些函数会在某个特定的时机由 Emacs 负责调用。如`write-file-hoos`会在 buffer 保存时调用。

* `progn` 用于把多个表达式合并为一个，从而用在如 if 从句里。

		(defun read-only-if-symlink ()
			(if (file-symlink-p buffer-file-name)
				(progn (setq buffer-read-only t)		￼		(message "File is a symlink"))))
* ` 'read-only-if-symlink)`
* 匿名函数和 `add-hook`
		(add-hook 'find-file-hooks 
				   '(lambda ()
						(if (file-symlink-p buffer-file-name)
							(progn
			￼				(setq buffer-read-only t)
			￼				(message "File is a symlink"))))

P35