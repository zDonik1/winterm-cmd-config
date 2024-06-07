# .dotfiles

## NixOS

The config is mainly written for NixOS, even though it didn't start that way. I prefer always working in NixOS now, since I can even use it in Windows with WSL2.

After installing NixOS:

```sh
cd ~
git clone .config https://github.com/zDonik1/.dotfiles.git
cd .config
sudo nixos-rebuild switch --flake ./nixos#wsl
```

## Windows

The only reason you might want the config in Windows is that WSL is not supported for some reason. The config was mainly written to be crossplatform before adding NixOS, but now it's supported on best effort basis.

Ensure that you have Visual Studio since the Telescope fzf native Neovim plugin should compile fzf.

Install scoop first and then run:

```powershell
cd $env:USERPROFILE
git clone .config https://github.com/zDonik1/.dotfiles.git
cd .config
install_packages.bat
```
