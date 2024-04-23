
# Atualização do Sistema e Instalação de algumas lib

```bash
sudo apt update && sudo apt upgrade -y && sudo apt install git curl -y
```

# Instalação do node

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"
```

```bash
nvm install 20 && nvm use 20 && node -v && npm -v 
```

# Configuracão PM2

- Veja a configuração do [PM2](PM2.md)