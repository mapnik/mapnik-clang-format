# mapnik-clang-format
Mapnik C/C++ style 

#### Emacs integration
```lisp
;; clang-format integration
;; set path to `clang-format`
(setq exec-path (append exec-path '("/opt/llvm/bin")))
(load "/opt/llvm/share/clang/clang-format.el")
(global-set-key [C-M-tab] 'clang-format-region)
(add-hook 'c++-mode-hook
	  '(lambda ()
	     (add-hook 'before-save-hook #'clang-format-buffer nil t)))
```
