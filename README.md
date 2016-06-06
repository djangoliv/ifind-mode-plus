# ifind-mode-plus

 A minor mode based on isearch, for interactively finding 
 
 
 Fork of ifind-mode [https://www.emacswiki.org/emacs/ifind-mode.el](https://www.emacswiki.org/emacs/ifind-mode.el):


 With this version you can
   * exclude files
   * exclude directories
   * switch between projects

## Configuration

``` emacs-lisp
(setq workspace-dir "~/workspaces/Proj1a ~/workspaces/Proj1b ~/workspaces/Proj2 ~/workspaces/Proj3")
(setq ifind-project-list '(("Proj1" . "~/workspaces/Proj1a ~/workspaces/Proj1b")
		                  ("Proj2" . "~/workspaces/Proj2")
                          ("Proj3" . "~/workspaces/Proj3")))
(setq ifind-excluded-dirs-list '(".git" ".svn"))
(setq ifind-excluded-files-list '("*.pyc" "*.o"))
(autoload 'ifind-mode "ifind-mode-plus" "" t)
(autoload 'ifind-switch-project "ifind-mode-plus" "" t)
(global-set-key (kbd "C-x F") 'ifind-mode)
(global-set-key (kbd "C-x S") 'ifind-switch-project)
```
## Other projects with the same goal
   * [https://github.com/bbatsov/projectile](projectile)
   * [https://github.com/technomancy/find-file-in-project](find-file-in-project)
   * [https://www.emacswiki.org/emacs/ifind-mode.el](ifind-mode)
   
## Why ifind-mode-plus
   * simple to configure
   * easy to use
   * no more than necessary

contributions are welcome !
