# Instruções: Como Jogar e Como Publicar no GitHub Pages

Este documento contém todas as orientações para jogar o **Jogo da Memória Multiplayer** (em modo Solo ou P2P) e o passo a passo completo para publicá-lo gratuitamente no **GitHub Pages**.

---

## 🎮 1. Como Jogar

O jogo conta com dois modos: **Modo Solo** e **Modo Multiplayer P2P em Tempo Real**.

### A. Modo Solo
Ideal para treinar a memória individualmente.
1. Clique na aba **"🎮 Modo Solo"** no topo.
2. Clique nas cartas para virá-las (máximo de 2 cartas por tentativa).
3. Ao encontrar duas cartas com o mesmo símbolo (ex: 🍎 e 🍎), o par é fixado e sua pontuação aumenta.
4. Se errar, as cartas viram de volta após um breve intervalo.
5. O objetivo é encontrar todos os **8 pares** no menor número de movimentos possíveis.

---

### B. Modo Multiplayer P2P (Dois Jogadores)
Jogue contra um amigo em tempo real, direto pelo navegador, sem necessidade de cadastro ou login.

#### Como Iniciar a Partida:
1. Clique na aba **"🌐 Multiplayer P2P"**.
2. Você pode escolher uma das duas opções:
   - **Criar Nova Sala**: Clique em **"✨ Criar Nova Sala Automática"**. O sistema gerará um código único (ex: `#sala-x9k2`).
   - **Entrar em Sala Existente**: Digite o nome da sala no campo de texto e clique em **"Entrar"** (ou pressione `Enter`).
3. Para convidar seu amigo, clique em **"🔗 Copiar Link de Convite"** e envie pelo WhatsApp, Discord ou Telegram.
4. Quando seu amigo abrir o link no navegador dele, o pareamento WebRTC acontecerá automaticamente e a luz de status mudará para **🟢 "Oponente conectado!"**.

#### Regras da Partida:
- **Turnos Alternados**: O jogador da vez terá sua carta e o banner destacados em verde (**"🌟 SUA VEZ DE JOGAR"**). Fora do seu turno, as cartas ficam bloqueadas para evitar conflitos de clique.
- **Acertou, joga de novo**: Se você encontrar um par, ganha 1 ponto e continua jogando a próxima jogada.
- **Errou, passa a vez**: Se virar cartas diferentes, as cartas desviram e a vez passa para o oponente.
- **Fim de Jogo**: Quando os 8 pares forem descobertos, o jogador com maior número de pares vence (com animação de confetes).
- **Revanche**: Qualquer jogador pode clicar em **"🔄 Reiniciar Partida"** ou **"Jogar Novamente"** para embaralhar um novo tabuleiro sincronizado para ambos.

---

## 🚀 2. Como Publicar no GitHub Pages

Por ser um projeto 100% estático (Jamstack), ele pode ser hospedado de forma totalmente gratuita e rápida no **GitHub Pages**.

### Passo 1: Enviar os arquivos para o repositório no GitHub
Abra o terminal no diretório do projeto e execute os comandos:

```bash
# 1. Adiciona todos os arquivos
git add .

# 2. Faz o commit das alterações
git commit -m "feat: multiplayer jamstack game with webrtc and instructions"

# 3. Envia para a branch principal (main ou master)
git push origin main
```

---

### Passo 2: Ativar o GitHub Pages nas Configurações

1. Acesse o seu repositório no [GitHub](https://github.com).
2. Clique na aba **Settings** (Configurações) no menu superior do repositório.
3. No menu lateral esquerdo, vá até a seção **Pages** (dentro do bloco *Code and automation*).
4. Na seção **Build and deployment**:
   - **Source**: Selecione `Deploy from a branch`.
   - **Branch**: Selecione a branch `main` (ou `master`) e mantenha a pasta como `/ (root)`.
   - Clique no botão **Save**.

---

### Passo 3: Acessar a URL Pública

1. Aguarde cerca de **1 a 2 minutos** enquanto o GitHub processa a publicação.
2. Atualize a página do *Settings > Pages*. Você verá uma mensagem de sucesso no topo:
   > *"Your site is live at https://<seu-usuario>.github.io/<nome-do-repositorio>/"*
3. Clique no link para abrir o jogo na internet!

---

### 💡 Dicas Importantes:
* **HTTPS Obrigatório**: O GitHub Pages já fornece certificado SSL (HTTPS) por padrão. O HTTPS é fundamental para que o navegador permita o uso da API de WebRTC e a cópia de links para a área de transferência (`navigator.clipboard`).
* **Jogando entre dispositivos**: Você pode abrir o link no computador e convidar um amigo no smartphone; o jogo é 100% responsivo e funciona em qualquer navegador moderno (Chrome, Edge, Safari, Firefox).
