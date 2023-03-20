# oh-my-zsh no MacOS

## Instalação oh-my-zsh
    curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh; zsh

## Instalação plugins
##### zsh-syntax-highlighting: basicamente vai deixar o comando verde se tiver sido digitado corretamente, ou do contrário, vermelho. E ao digitar um caminho, ele ficará sublinhado caso o arquivo/diretório existir.
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

##### zsh-autosuggestions: vai sugerir comandos baseados no seu histórico.
    git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

## Habilitar plugins instalados dentro de plugins=(git) em ~/.zshrc
    (git dnf zsh-syntax-highlighting zsh-autosuggestions)
## Rodar comando para alterar o shell padrão do usuário para o Zsh
    zsh
    chsh -s $(which zsh)

## Instalação buscador em arquivo digite a palavra e CTRL + T
    git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install

## Instalação fonte nerd
    curl -fLo /tmp/nerd-fonts.zip https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/SourceCodePro.zip
    unzip -o /tmp/nerd-fonts.zip -d ~/Library/Fonts/

  Alterar fonte no terminal manualmente

## Instalação tema powerlevel10k
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

### Alterar manualmente ~/.zshrc
    ZSH_THEME="powerlevel10k/powerlevel10k"