# First steps

You need to clone this repository and go to the /tmp/ directory

```
git clone https://github.com/dt-wark/dotfiles.git /tmp/dotfiles && cd /tmp/dotfiles
```

# Shell (ZSH)

- **Theme**: [**`gentoo`**](https://github.com/ohmyzsh/ohmyzsh/blob/master/themes/gentoo.zsh-theme)
- **Installed plug-ins**: [**`colored-man-pages`**](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/colored-man-pages) [**`zsh-autosuggestions`**](https://github.com/zsh-users/zsh-autosuggestions) [**`zsh-syntax-highlighting`**](https://github.com/zsh-users/zsh-syntax-highlighting)

![zsh screenshot](https://res.cloudinary.com/wark/image/upload/v1590752586/zsh.png)


### Let's install zsh and change the standard shell

##### Step by step

```
sudo apt update
sudo apt upgrade -y
sudo apt install zsh
sudo apt-get install powerline fonts-powerline
git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
mv shell/zshrc ~/.zshrc
chsh -s /usr/bin/zsh
```

##### Or one line

```sudo apt update && sudo apt upgrade -y && sudo apt install zsh -y && sudo apt-get install powerline fonts-powerline -y && git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions && git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting && mv shell/zshrc ~/.zshrc && chsh -s /usr/bin/zsh```


### Aliases and virtual environment variables

```
cd /tmp/dotfiles
mv shell/shell_aliases ~/.shell_aliases
mv shell/shell_env ~/.shell_env
```

### pfetch
pfetch is configured via [environment variables](https://github.com/dylanaraps/pfetch#configuration)
a couple of variables are already set in `.shell_env`
```
git clone https://github.com/dylanaraps/pfetch.git
sudo install pfetch/pfetch /usr/local/bin/
```


# Vim

- **Theme**: [**`Oceanic Next`**](https://github.com/mhartington/oceanic-next)
- **Plugin Manager**: [**`Vundle`**](https://github.com/VundleVim/Vundle.vim)
- **Installed plug-ins**: [**`nerdtree`**](https://github.com/preservim/nerdtree)

![vim screenshot](https://res.cloudinary.com/wark/image/upload/v1590686044/vim.png)

- **`Relative numbers are enabled`**
- **`Disabled automatic commenting on new line`**
- **`Backups and swap files are disabled`**
- **`Splits are opened at the bottom and right and the navigation keys are remapped`**
- **`The new tab is aliased to Ctrl+t`**
- **`Global replace is aliased to S`**
- **`System clipboard by default`**
- **`Spellchecker is aliased to F5`**
- **`UTF-8 by default`**

In general, my `.vimrc` is configured to work with Python: syntax is highlighted, indents are set to 4 spaces, smart indentation after keywords is enabled.

### Let's install Vundle, the color scheme and our configuration files

##### Step by step

```
mkdir ~/.vim
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
mv vim/vimrc ~/.vimrc
mv -v vim/colors/ vim/spell/ ~/.vim/
vim +PluginInstall +qall
```

##### Or one line

```
mkdir ~/.vim && git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim && mv vim/vimrc ~/.vimrc && mv -v vim/colors/ vim/spell/ ~/.vim/ && vim +PluginInstall +qall
```

And that's it!

