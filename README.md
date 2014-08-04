Emium - The Emacs abuser's browser
=============================

[![Build Status](https://secure.travis-ci.org/darth10/emium.png?branch=master)](https://travis-ci.org/darth10/emium)

Emium is a fork of the [Vimium](https://github.com/philc/vimium) Chrome extension which provides Emacs key bindings for navigation and control.

Note that the key bindings do not completely match Emacs.
The objective of this project is to find hybrid set of browser key bindings that provide the aesthetics of Emacs.
Feel free to open an issue and contribute.

__Installation instructions:__

*TODO*

You can install the stable version of Emium from the
[Chrome Extensions Gallery](https://chrome.google.com/extensions/detail/dbepggeogbaibhgnhhndojpepiihcmeb).

Please see
[CONTRIBUTING.md](https://github.com/philc/vimium/blob/master/CONTRIBUTING.md#installing-from-source)
for instructions on how you can install Emium from source.

The Options page can be reached via a link on the help dialog (hit `?`) or via the button next to Emium on
the Chrome Extensions page (`chrome://extensions`).

Keyboard Bindings
-----------------

Modifier keys are specified as `<c-x>`, `<m-x>`, and `<a-x>` for ctrl+x, meta+x, and alt+x
respectively. See the next section for instructions on customizing these bindings.

Navigating the current page:

    ?       show the help dialog for a list of all available keys
    n       scroll down
    p       scroll up
    v       scroll down
    <a-v>   scroll up
    b       scroll left
    f       scroll right
    a       scroll all the way left
    e       scroll all the way right
    <       scroll to top of the page
    >       scroll to bottom of the page
    }       scroll down half a page
    {       scroll up half a page
    !       reload
    j       open a link in the current tab
    uj      open a link in a new tab
    <a-q>   open multiple links in a new tab
    <a-l>   copy a link url to the clipboard
    <a-w>   copy the current url to the clipboard
    y       open copied url in the current tab
    uy      open copied url in a new tab
    ur      cycle forward to the next frame
    us      view source
    i       enter insert mode
    ESC     enter normal mode

Navigating to new pages:

    u<a-j>  Open URL, bookmark, or history entry
    <a-j>   Open URL, bookmark, history entry in a new tab
    u<a-o>  Open bookmark
    <a-o>   Open bookmark in a new tab

Using find:

    <a-s>   enter find mode -- type your search query and hit enter to search or esc to cancel
            See here for advanced usage (regular expressions): https://github.com/philc/vimium/wiki/Find-Mode
    s       cycle forward to the next find match
    r       cycle backward to the previous find match

Navigating your history:

    <a-p>   go back in history
    <a-n>   go forward in history

Manipulating tabs:

    ub         go one tab left
    uf         go one tab right
    ua         go to the first tab
    ue         go to the last tab
    t          create tab
    ut         duplicate current tab
    w          close current tab
    uw         restore closed tab (i.e. unwind the 'w' command)
    k          move tab to new window
    uk         pin/unpin current tab
    <a-b>      move tab left
    <a-f>      move tab right
    <a-j>      search through your open tabs

Additional advanced browsing commands:

    ]]      Follow the link labeled 'next' or '>'. Helpful for browsing paginated sites.
    [[      Follow the link labeled 'previous' or '<'. Helpful for browsing paginated sites.
    ui      focus the first (or n-th) text input box on the page
    <a-a>   go up one level in the URL hierarchy
    <a-r>   go up to root of the URL hierarchy

Emium supports command repetition so, for example, hitting '5t' will open 5 tabs in rapid succession. `<ESC>` (or
`<c-[>`) will clear any partial commands in the queue and will also exit insert and find modes.

There are some advanced commands which aren't documented here. Refer to the help dialog (type `?`) for a full
list.

Custom Key Mappings
-------------------

You may remap or unmap any of the default key bindings in the "Key mappings" section under "Advanced Options"
on the options page.

Enter one of the following key mapping commands per line:

- `map key command`: Maps a key to a Emium command. Overrides Chrome's default behavior (if any).
- `unmap key`: Unmaps a key and restores Chrome's default behavior (if any).
- `unmapAll`: Unmaps all bindings. This is useful if you want to completely wipe Emium's defaults and start
  from scratch with your own setup.

Examples:

- `map <c-d> scrollPageDown` maps ctrl+d to scrolling the page down. Chrome's default behavior of bringing up
  a bookmark dialog is suppressed.
- `map r reload` maps the r key to reloading the page.
- `unmap <c-d>` removes any mapping for ctrl+d and restores Chrome's default behavior.
- `unmap r` removes any mapping for the r key.

Available Emium commands can be found via the "Show Available Commands" link near the key mapping box. The
command name appears to the right of the description in parenthesis.

You can add comments to your key mappings by starting a line with `"` or `#`.

The following special keys are available for mapping:

- `<c-*>`, `<a-*>`, `<m-*>` for ctrl, alt, and meta (command on Mac) respectively with any key. Replace `*`
  with the key of choice.
- `<left>`, `<right>`, `<up>`, `<down>` for the arrow keys
- `<f1>` through `<f12>` for the function keys

Shifts are automatically detected so, for example, `<c-&>` corresponds to ctrl+shift+7 on an English keyboard.

Contributing
------------
Please see [CONTRIBUTING.md](https://github.com/philc/vimium/blob/master/CONTRIBUTING.md) for details.

Release Notes
-------------

*TODO*

License
-------

*TODO*
