# auto-virtualenvwrapper

Automatically activates python virtualenv on emacs using:

* `python-version` file in the project root.
* `.venv` or `venv` directory (or link) in the project root.
* Try find a virtualenv with the same name of Project Root.

Project root is defined as a parent directory containing `auto-virtualenvwrapper-project-root-files`. By default the variable equals to `(".python-version" ".dir-locals.el" ".projectile" ".emacs-project" "manage.py" ".git" ".hg")`.

This code is based on [auto-virtualenv](https://github.com/marcwebbie/auto-virtualenv), but uses tiny [virtualenvwrapper](https://github.com/porterjamesj/virtualenvwrapper.el) library rather then [pyenv](https://github.com/jorgenschaefer/pyvenv). This way you avoid additional dependencies: pyenv and elpy.


## Installation


### MELPA

TBD. Waiting for adding the package to the melpa repository.

<!-- `auto-virtualenvwrapper` is available on [MELPA](https://melpa.org). -->

<!-- You can install `auto-virtualenvwrapper` with the following command. -->

<!-- <kbd>M-x package-install [RET] auto-virtualenvwrapper [RET]</kbd> -->

### manual

Clone this repository somewhere and add this directory to you
`load-path`.

## Usage

```elisp
(require 'auto-virtualenvwrapper)
(add-hook 'python-mode-hook #'auto-virtualenvwrapper-activate)
```

Optionally:

```elisp
;; Activate on changing buffers
(add-hook 'window-configuration-change-hook #'auto-virtualenvwrapper-activate)
;; Activate on focus in
(add-hook 'focus-in-hook #'auto-virtualenvwrapper-activate)
```

## Alternatives

+ [auto-virtualenv](https://github.com/marcwebbie/auto-virtualenv)
+ [pyenv-mode-auto](https://github.com/ssbb/pyenv-mode-auto)

## License

[![GNU GPL v3.0](http://www.gnu.org/graphics/gplv3-127x51.png)](http://www.gnu.org/licenses/gpl.html)

View official GNU site <http://www.gnu.org/licenses/gpl.html>.
