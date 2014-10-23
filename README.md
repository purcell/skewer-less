[![Melpa Status](http://melpa.org/packages/skewer-less-badge.svg)](http://melpa.org/#/skewer-less)
[![Melpa Stable Status](http://stable.melpa.org/packages/skewer-less-badge.svg)](http://stable.melpa.org/#/skewer-less)

skewer-less.el
==============

Emacs minor mode allowing [LESS](http://lesscss.org) stylesheet
manipulation via [skewer-mode](https://github.com/skeeto/skewer-mode).

Note that this is intended for use in place of `skewer-css-mode`,
which does not work with `LESS`.

Operates by invoking `less.refresh()` via skewer on demand, or
whenever the buffer is saved.

For this to work properly, the `less` javascript should be included
in the target web page, and `less` should be configured in
development mode, e.g.

```html
<script>
  var less = {env: "development"};
</script>
<link href="/stylesheets/application.less" rel="stylesheet/less">
<script src="/path/to/less.js" type="text/javascript"></script>
```

I may consider providing an option to instead run `lessc` from
Emacs, then send the output via skewer-css. Let me know if you want this.

Installation
=============

If you choose not to use one of the convenient
packages in [Melpa][melpa] and [Marmalade][marmalade], you'll need to
add the directory containing `skewer-less.el` to your `load-path`, and
then `(require 'skewer-less)`.

Usage
=====

Enable `skewer-less` in an individual buffer like this:

```lisp
(skewer-less-mode)
```

Save the buffer to trigger an update, or hit <kbd>C-c C-k</kbd> just
like in `skewer-css-mode`.

[marmalade]: http://marmalade-repo.org
[melpa]: http://melpa.org

<hr>

[![](http://api.coderwall.com/purcell/endorsecount.png)](http://coderwall.com/purcell)

[![](http://www.linkedin.com/img/webpromo/btn_liprofile_blue_80x15.png)](http://uk.linkedin.com/in/stevepurcell)

[Steve Purcell's blog](http://www.sanityinc.com/) // [@sanityinc on Twitter](https://twitter.com/sanityinc)
