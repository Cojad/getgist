# GetGist

This is a simple script I wrote to easily download any file from a public [GitHub Gist](http://gist.github.com) account.

For some reason I do not have a `dotfile` repository because I prefer to store my `.vimrc`, `.gitconfig`, `.bash*` etc. as gists.

## Installing

Just copy the `getgist.py` to the directory where you want to have your files downloaded.

## Usage

Just run `python getgist.py <user> <file>`. For example:

```
vagrant@vagrant ~ $ python getgist.py cuducos .vimrc
  Fetching https://gist.github.com/cuducos ...
  Fetching https://gist.github.com/cuducos/409fac6ac23bf515f495 ...
  Fetching https://gist.github.com/cuducos/409fac6ac23bf515f495/raw/cd76d11be3973c887cd299785569c5159701d339/.vimrc ...
  Replace existing .vimrc ? (y/n) y
  Deleting existing .vimrc …
  Saving new .vimrc …
  Done!
vagrant@vagrant ~ $
```

If you decide **not to delete** your copy of the local file, the **local file is renamed** with an extension such as `.bkp`, `.bkp.1`, `.bkp.2` etc.

## To do list

* Distribute it as standard PyPI package
* Make it a CLI command (e.g. `$ getgist cuducos .vimrc`)
* Store default user (e.g. `$ getgist .vimrc` to download my `.vimrc` but `$ getgist johndoe .vimrc` to download John's one)

## License

So far I consider this script just public domain.