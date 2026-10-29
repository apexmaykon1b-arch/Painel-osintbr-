# 🔎 PAINEL OSINT BR
Um painel completo de **Open Source Intelligence (OSINT)** desenvolvido para automatizar a busca, coleta e correlação de informações em fontes abertas diretamente pelo ecossistema do **Termux**.

<p align="center">
  <!-- Se você quiser, pode subir um print do seu menu no GitHub e colocar o link dele aqui embaixo para aparecer uma foto na página inicial -->
  <!-- <img src="link_da_sua_imagem.png" alt="Menu Principal"> -->
</p>

## 🚀 O que o painel faz?
O **Painel OSINT BR** unifica múltiplas ferramentas de investigação digital e recon em um menu interativo, rápido e prático para o terminal:

* **1. E-mail (Formato + MX):** Valida a estrutura de e-mails e consulta registros MX para verificar a existência real do servidor em cerca de **80 plataformas diferentes**.
* **2. Username (Sherlock-style):** Varredura avançada para identificar a presença de um nome de usuário em uma lista massiva de mais de **88 redes sociais e fóruns** (incluindo Instagram, Facebook, Telegram, etc.).
* **3. Telefone:** Padronização, normalização e identificação de metadados de números telefônicos.
* **4. DNS & 5. HTTP(S):** Reconhecimento de infraestrutura web, colhendo registros de domínios, status de respostas e cabeçalhos HTTP.
* **6. IP Público:** Geolocalização e informações estimadas de provedores (ASN) a partir de um IP de destino.
* **7. Portas TCP:** Scanner focado em mapeamento rápido de até **100 portas TCP comuns**.
* **8. Arquivo (Metadados + SHA-256):** Extração de dados ocultos (Exif/metadados) em documentos e geração de assinaturas criptográficas hash.
* **9. Resultados, Exportação (JSON) & Extrator Intel:** Histórico unificado com capacidade para correlacionar inteligência coletada (E-mail, IP, URL, Hash, CPF) e exportar relatórios estruturados prontos para análise.

---

## 📲 Guia de Instalação no Termux

Copie e cole as linhas de comando abaixo no seu terminal para preparar o ambiente, baixar o repositório, instalar todas as dependências do Python e executar a ferramenta de forma correta:

```bash
# 1. Atualizar as listas do sistema e pacotes do Termux
pkg update && pkg upgrade -y

# 2. Instalar as ferramentas nativas necessárias (Git, Unzip e Python)
pkg install git unzip python -y

# 3. Clonar o repositório oficial do projeto
git clone https://github.com

# 4. Entrar na pasta do repositório
cd Painel-osintbr-

# 5. Extrair o arquivo compactado da versão atual
unzip painel-osintbr-v1.5-cobertura-ampliada.zip

# 6. Mudar para o diretório interno descompactado
cd painel-osintbr-v1.5-cobertura-ampliada

# 7. Instalar as bibliotecas e dependências do Python necessárias
pip install --upgrade pip
pip install requests colorama beautifulsoup4 urllib3

# 8. Executar a ferramenta
python main.py
```

---

## ⚠️ Isenção de Responsabilidade (Disclaimer)
Esta ferramenta foi desenvolvida exclusivamente para fins educacionais, de pesquisa em fontes abertas (OSINT) e auditoria de segurança autorizada. O uso deste software para atividades ilícitas, invasão de privacidade ou sem o consentimento explícito dos alvos é de total responsabilidade do usuário final. O desenvolvedor não se responsabiliza por quaisquer danos ou uso indevido da ferramenta.
