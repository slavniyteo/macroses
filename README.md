# Macroses

Easy way to manage your macroses in linux

Macroses is a couple of shell scripts which allow to simply create and manage your macroses.

For example, if you usially use `grep` for full-text search and don't want to type againt and again `grep -d recurce -e pattern`, you just add new macros:

```sh
echo 'grep -d recurse -e pattern' | macros-add grep-dit
```

Oh no! You misstyped and need to rename your macros? Dont panic! Just do:

```sh
macros-mv grep-dit grep-dir
```

Want to copy-paste and modify?

```sh
macros-cp grep-dir grep-dir-copy
```

Or delete?

```sh
macros-rm grep-dir-copy
```

You may also list all you macroses with `macros-ls` and grep them:

```sh
macros-ls grep-d
```

And print them
```sh
macros-cat grep-dir
```

Or edit with vim:
```sh
macros-vim grep-dir
```

That's all. Enjoy =)

# Install

1. Create a direcory to store macroses and copy there all files from .macroses directory
2. Add this directory to **MACROSES_HOME** environment variable;
3. Add **$MACROSES_HOME** to **$PATH** variable;
4. ...
5. PROFIT!

For example:
```sh
mkdir ~/.macroses_dir
cp ./microses/* ~/.macroses_dir/
echo 'MICROSES_HOME=~/.macroses_dir' >>~/.profile
echo 'PATH="$PATH:$MICROSES_HOME"' >>~/.profile
```

# Bash completion

You may want to make bash autocomplete your macros names. Just copy file `./bash_completion/macroses` to `/etc/bash_completion.d` and login/logout.

