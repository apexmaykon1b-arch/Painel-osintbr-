## 📲 Guia de Instalação

A ferramenta usa **apenas a biblioteca padrão do Python**. Não precisa de `pip` nem de ambiente virtual (venv). Copie e cole os comandos do seu sistema, um bloco por vez.

### 🤖 Termux (Android)

```bash
pkg update && pkg upgrade -y
pkg install git unzip python -y
termux-setup-storage   # opcional: só se o ZIP estiver em Downloads
cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-.git
cd Painel-osintbr-
unzip -o painel-osintbr-v1.5-cobertura-ampliada.zip
cd painel-osintbr-v1
python main.py
```

> ZIP em Downloads? Troque o `unzip` por:
> `unzip -o ~/storage/downloads/painel-osintbr-v1.5-cobertura-ampliada.zip`

### 🐧 Debian, Ubuntu, Kali e Parrot

```bash
sudo apt update && sudo apt install -y git unzip python3
cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-.git
cd Painel-osintbr-
unzip -o painel-osintbr-v1.5-cobertura-ampliada.zip
cd painel-osintbr-v1
python3 main.py
```

### 🎩 Fedora e Arch

```bash
# Fedora: sudo dnf install -y git unzip python3
# Arch:   sudo pacman -S --needed git unzip python
cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-.git
cd Painel-osintbr-
unzip -o painel-osintbr-v1.5-cobertura-ampliada.zip
cd painel-osintbr-v1
python3 main.py
```

### 🍎 macOS

```bash
xcode-select --install   # se pedir; já inclui git e python3
cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-.git
cd Painel-osintbr-
unzip -o painel-osintbr-v1.5-cobertura-ampliada.zip
cd painel-osintbr-v1
python3 main.py
```

### 🪟 Windows (PowerShell)

```powershell
winget install --id Git.Git -e
winget install --id Python.Python.3.12 -e
# feche e abra o PowerShell novamente, depois:
cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-.git
cd Painel-osintbr-
Expand-Archive -Force painel-osintbr-v1.5-cobertura-ampliada.zip .
cd painel-osintbr-v1
python main.py
```

> Usa WSL ou Git Bash? Siga o bloco de Debian/Ubuntu.

### ✅ Testar a instalação

Dentro da pasta `painel-osintbr-v1`:

```bash
python3 -m unittest discover -s tests -v   # no Termux e no Windows use: python
```

### 🔄 Atualizar

```bash
cd ~/Painel-osintbr-
git pull
cp -r painel-osintbr-v1/data ~/osintbr-backup-data 2>/dev/null   # guarda seu banco local
unzip -o painel-osintbr-v1.5-cobertura-ampliada.zip
```

> ℹ️ O banco fica em `data/osintbr.sqlite3` e as exportações em `exports/`. Não publique exportações com dados sensíveis.

### 🛠️ Problemas comuns

| Erro | Solução |
|---|---|
| `python: command not found` | Instale o Python (`pkg install python`, `apt install python3`, etc.). No Linux/macOS use `python3`. |
| `main.py` não encontrado | Rode `pwd` e `ls`. Entre na pasta `painel-osintbr-v1`, que tem `main.py` e `core/`. |
| `unzip: command not found` | Instale o `unzip` (`pkg install unzip` ou `sudo apt install unzip`). |
| `git clone` falha | Confira a internet e se o endereço está correto. |
| Timeout nas consultas | Verifique a conexão. O erro não prova que o alvo não existe. |
