## Neovim Config
My config for Neovim


### Instaling Neovim
```
sudo apt update
sudo apt upgrade
sudo apt install curl git neovim
```

### Installing Vim-Plug for Neovim
```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

### Binding Neovim to ```v```
```
echo "alias v='vim'" >> ~/.bashrc
source ~/.bashrc
```

### Installing the Config
```
mkdir -p ~/.config/nvim/
wget https://raw.githubusercontent.com/Drew-Alleman/neovim/main/init.vim -O ~/.config/nvim/init.vim
```
Then once the config is set, open neovim and run ```PlugInstall```. 

## Gnome Extensions
https://extensions.gnome.org/extension/3088/extension-list/ - Simple GNOME Shell extension manager in the top panel <br>
https://extensions.gnome.org/extension/8/places-status-indicator/ - Add a menu for quickly navigating places in the system.<br>
https://extensions.gnome.org/extension/1007/window-is-ready-notification-remover/ - Removes window is ready Notification<br>
https://extensions.gnome.org/extension/1036/extensions/ - Enable/disable easily gnome shell extensions from a menu in the top panel. Also allows to edit the settings of the extensions. Feedback welcome!<br>
https://extensions.gnome.org/extension/3960/transparent-top-bar-adjustable-transparency/ - Bring back the transparent top bar in GNOME Shell with adjustable transparency.<br>
https://extensions.gnome.org/extension/4679/burn-my-windows/ - Disintegrate your windows with style. <br>

## Setting Up Desktop Icons
### Creating The Applications desktop file
```
vim ~/.local/share/applications/mGBA.desktop
```
```
[Desktop Entry]
Name=mGBA
Exec=/home/drew/Applications/mGBA-0.10.2-appimage-x64.appimage
Icon=/home/drew/Pictures/Icons/Mgba-logo.png
Type=Application
Terminal=false
Categories=Game;Emulator;
```
### Making it executable and Creating the Desktop Icon
```
chmod +x ~/.local/share/applications/mGBA.desktop
ln -s ~/.local/share/applications/mGBA.desktop ~/Desktop/
```
