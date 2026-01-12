# Snippets

My personal collection for yasnippet

Setup:

```Text
ghq get git@github.com:ashishrv/snippets.git
ghq list --full-path
ln -s $HOME/personal/workspace/vcs/github.com/ashishrv/snippets/snippets  ~/.emacs.d/snippets
```

Now add this to init.el::

```lisp
(use-package yasnippet
  :ensure t ; Installs the package if not already installed
  :init
  (add-to-list 'yas-snippet-dirs "~/personal/workspace/vcs/github.com/ashishrv/snippets/snippets") ; Specify your custom directory
  :config
  (yas-reload-all)
  (yas-global-mode 1) ; Enables yasnippet globally
  ;; Alternatively, use a hook to enable it only in specific modes for lazy loading
  ;; (add-hook 'prog-mode-hook #'yas-minor-mode)
  ;; (add-hook 'text-mode-hook #'yas-minor-mode)
  )
```
