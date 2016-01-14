# VimFx Config template

[VimFx] can optionally be customized by a [config file].

This is the boilerplate needed to set it up.

- config.js is you actual config file.
- frame.js is needed if you add custom commands that access web page content.
- The rest of the files are there to get config.js and frame.js up and running.
  You don’t need to touch them (but advanced users can for maximum
  customizability).

[VimFx]: https://github.com/akhodakivskiy/VimFx/
[config file]: https://github.com/akhodakivskiy/VimFx/blob/master/documentation/config-file.md


## Setup

1. [Download all files as a .zip][download] and extract it. That should result
   in a directory called `VimFx-config--vimfx.org` containing seven files.
   Rename `VimFx-config--vimfx.org` to `VimFx-config@vimfx.org`. (Github don’t
   allow `@` in their .zip names.)

2. Find the `extensions` directory in your [profile directory].

3. Move the `VimFx-config@vimfx.org` directory into the extensions directory.

That’s it! To check if it works:

1. Restart Firefox.

2. Open the [browser console]. You should see the message “Hello, World! This is
   vimfx:” followed by an inspection of VimFx’s public API.

**Note:** Since Mozilla added [extension signing] things have gotten a bit more
complicated.

Now check out the [config file] documentation to get started customizing!

[download]: https://github.com/lydell/VimFx-config/archive/@vimfx.org.zip
[profile directory]: https://support.mozilla.org/en-US/kb/profiles-where-firefox-stores-user-data
[browser console]: https://developer.mozilla.org/en-US/docs/Tools/Browser_Console
[extension signing]: https://wiki.mozilla.org/Addons/Extension_Signing
[config file]: https://github.com/akhodakivskiy/VimFx/blob/master/documentation/config-file.md


## Tips

If you’d like to put your config file somewhere else, you can! There are two
ways to go:

- Create a plain text file called `VimFx-config@vimfx.org` in the extensions
  directory (a [proxy file]). Put the absolute path to your config file
  directory inside it, such as `/home/you/.vimfx/` or `C:\users\you\vimfx\`.

- Use a symlink. For example:

  ```
  ln -s /home/you/.vimfx/ /home/you/.mozilla/firefox/dgof8r37.default/extensions/VimFx-config@vimfx.org
  ```

[proxy file]: https://developer.mozilla.org/en-US/Add-ons/Setting_up_extension_development_environment#Firefox_extension_proxy_file
