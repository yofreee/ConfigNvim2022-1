## My Theme Color

![App Screenshot](https://i.postimg.cc/SK2p66kh/118175481-27755c80-b3fe-11eb-9d70-85a9f936c33d.png)

**If you are using Vim-Plug**
```Terminal
Plug 'shaunsingh/moonlight.nvim'
```
**Vim-Script:**
```Terminal
colorscheme moonlight
```

#
Installation and more about Moonlight in the following repository: https://github.com/shaunsingh/moonlight.nvim





#
## My Neovim setup
The complete configuration can be found in my init.vim file:
https://github.com/yofreee/ConfigNvim/blob/main/init.vim
#

## Install PIP
```Terminal
sudo pacman -S python3-pip (ArchCraft)
sudo apt-get install python3-pip (Ubuntu)
```

## No "python3" provider found. Run :checkhealth provider
This error is very common when wanting to code python in neovim, so from the terminal we must execute the following command:
#

```Terminal
python3 -m pip install --user --upgrade pynvim
```
#    
## Cannot write buftype option is set / Neovim - Vim
This is another common error that is fixed with the following command when Neovim or Vim is in "command mode":
```Neovim / Vim command mode
:set buftype=""
```

## Servers link for languages installed from Coc
https://github.com/neoclide/coc.nvim/wiki/Language-servers#java

## Extensiones para Neovim con Coc
https://github.com/neoclide/coc.nvim/wiki/Using-coc-extensions

## Plugins needed to install neovim correctly
- Have node and nodejs installed
- Have npm installed
- Have pip installed

## Telescope

**sudo pacman -S ripgrep**    (ripgrep is a line-oriented search tool that recursively searches the current directory for a regex pattern)
#
https://github.com/sharkdp/fd#installation
**sudo pacman -S fd** = ArchLinux (fd is a program to find entries in your filesystem)

**sudo apt install fd-find** = Ubuntu y otras distribuciones basadas en Debian
#
Agregue un enlace fd ejecutando el comando
```Terminal
ln -s $(which fdfind) ~/.local/bin/fd
```
para poder usarlo fd de la misma manera que en esta documentación. Asegúrate de que $HOME/.local/bin esté en tu $PATH.
#
**pip3 install tree_sitter**

#
## Instalación/Actualización nodejs
Mediante nvm y la versión más estable de nodejs
```Terminal
nvm install v(numero de versión)
```
Ej: nvm install v16.15.1

## Instalación npm
```Terminal
sudo apt install npm
```
## Instalación yarn
Instalar yarn de acuerdo a su sistema operativo o su preferencia pero instalarlo
```Terminal
curl --compressed -o- -L https://yarnpkg.com/install.sh | bash
```

## Neovim COC - "node is not executable"
Dentro de su init.vim o .vimrc encontrará la siguiente instrucción:
```Terminal
let g:coc_node_path = 'ruta de node'
```
El error puede ser causado por que la ruta que tiene let g:coc_node_path es incorrecta de acuerdo al sitio en donde su node se instalo, por lo tanto con el siguiente comando sabremos en que ruta se encuentra:
```Terminal
nvm which current
```
De allí, obtendremos una ruta la cual copiaremos y la reemplazaremos por la que tiene la variable let g:coc_node_path dentro de su init.vim o su .vimrc, ejemplo:
```Terminal
let g:coc_node_path = 'ruta resultante del anterior comando dentro de comillas simples'
```
## Instalar servidores de lenguaje
Coc aqui: https://github.com/neoclide/coc.nvim/wiki/Language-servers#supported-features
## Instalar extensiones para Neovim con Coc
https://github.com/neoclide/coc.nvim/wiki/Using-coc-extensions
#
# INFO: 'g:python3_host_prog' is not set
![App Screenshot](https://i.postimg.cc/c4JVj06J/pythonerror1.png)
Debemos buscar la ubicación de python3 mediante el siguiente comando:
```Terminal
which python3
```
y reemplazados dicha ruta en el init.vim o .vimrc
```Terminal
let g:python3_host_prog = 'ruta que resulto del anterior comando'
```
![App Screenshot](https://i.postimg.cc/jqJD009R/python3errorsolution.png)
