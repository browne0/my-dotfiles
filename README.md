# Malik’s dotfiles

## Installation

**Warning:** If you want to give these dotfiles a try, you should first fork this repository, review the code, and remove things you don’t want or need. Don’t blindly use my settings unless you know what that entails. Use at your own risk!

### Using Git and the bootstrap script

You can clone the repository wherever you want. (I like to keep it in `~/git/my-dotfiles`.) The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/browne0/my-dotfiles.git && cd my-dotfiles && source bootstrap.sh
```

To update, `cd` into your local `my-dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

### Specify the `$PATH`

If `~/.path` exists, it will be sourced along with the other files, before any feature testing (such as [detecting which version of `ls` is being used](https://github.com/mathiasbynens/dotfiles/blob/aff769fd75225d8f2e481185a71d5e05b76002dc/.aliases#L21-L26)) takes place.

Here’s an example `~/.path` file that adds `/usr/local/bin` to the `$PATH`:

```bash
export PATH="/usr/local/bin:$PATH"
```

## Feedback

Suggestions/improvements
[welcome](https://github.com/browne0/my-dotfiles/issues)!

## Thanks to…

[![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](http://twitter.com/mathias) Mathias Bynens and [his dotfiles configuration](https://github.com/mathiasbynens/dotfiles) that gave me inspiration and a place to start!
