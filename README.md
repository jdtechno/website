Haiku Project website
======================================
This repository contains the source code for Haiku's main website.

## Blogging
To create a brand new blog for a new user, run `./scripts/newblog.sh`.

To create a brand new blogpost, run `./scripts/newpost.sh`.

Refer Troubleshooting section if you encounter any error.

## Shortcodes
Shortcodes introduce the power to leverage special formatting
in markdown documents. All available shortcodes are in layouts/shortcodes.

### Alerts
A classic alert or notification div with a title and a body

 * ``{{< alert-danger "Title" "Body text here">}}``
 * ``{{< alert-warning "Title" "Body text here">}}``
 * ``{{< alert-info "Title" "Body text here">}}``

### Keyboard
A small keyboard like span. Normally wont to represent pressing
a physical key on the keyboard.

 * ``{{< keyboard ALT >}}``

## Troubleshooting

### macOS: "date: illegal option"

This is because OS X/macOS and Linux use two different sets of tools. Linux uses the GNU version of the date command (hence, GNU/Linux). the answer would be to install GNU Core Utilities replacing macOS Utilities:

*Homebrew:*

``brew install coreutils``

*MacPorts*

``sudo port install coreutils``

Set your PATH to: ``PATH="/usr/local/opt/coreutils/libexec/gnubin:$PATH"``

Run ``which date``, it must show ``/usr/local/opt/coreutils/libexec/gnubin/date`` and not ``/bin/date``. Re-run the above command, it should work fine!
