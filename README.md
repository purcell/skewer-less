[![Melpa Status](http://melpa.org/packages/skewer-less-badge.svg)](http://melpa.org/#/skewer-less)
[![Melpa Stable Status](http://stable.melpa.org/packages/skewer-less-badge.svg)](http://stable.melpa.org/#/skewer-less)
<a href="https://www.patreon.com/sanityinc"><img alt="Support me" src="https://img.shields.io/badge/Support%20Me-%F0%9F%92%97-ff69b4.svg"></a>

skewer-less.el
==============

Emacs minor mode allowing [LESS](http://lesscss.org) stylesheet
manipulation via [skewer-mode](https://github.com/skeeto/skewer-mode).

Note that this is intended for use in place of `skewer-css-mode`,
which does not work with `LESS`.

The LESS styles in the current buffer will be passed through `lessc`
and then to `skewer-css`.  For this to work properly, the `lessc`
command should be present on `exec-path`.

Installation
=============

If you choose not to use one of the convenient packages in
[MELPA][melpa], you'll need to add the directory containing
`skewer-less.el` to your `load-path`, and then `(require
'skewer-less)`.

Usage
=====

Enable `skewer-less` in an individual buffer like this:

```elisp
(skewer-less-mode)
```

Alternatively, add `'skewer-less-mode` to your `less-css-mode-hook`:

```elisp
(add-hook 'less-css-mode-hook 'skewer-less-mode)
```

Save the buffer to trigger an update, or hit <kbd>C-c C-k</kbd> just
like in `skewer-css-mode`.

[melpa]: http://melpa.org

<hr>

[![](http://api.coderwall.com/purcell/endorsecount.png)](http://coderwall.com/purcell)

[![](http://www.linkedin.com/img/webpromo/btn_liprofile_blue_80x15.png)](http://uk.linkedin.com/in/stevepurcell)

[Steve Purcell's blog](http://www.sanityinc.com/) // [@sanityinc on Twitter](https://twitter.com/sanityinc)
