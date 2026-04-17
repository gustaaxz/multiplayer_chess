# ♞ Xadrez Premium Online

![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

Bem-vindo ao **Xadrez Multiplayer**! Um simulador de xadrez moderno e responsivo, focado em oferecer uma experiência competitiva de alta qualidade diretamente no navegador, com suporte a partidas locais, contra IA e multiplayer em tempo real.

---

## 🎮 Modos de Jogo

O sistema oferece três maneiras distintas de jogar, selecionáveis no menu principal:

### 1. 🤝 Jogar Local (2 Jogadores)
Ideal para jogar com alguém fisicamente ao seu lado, utilizando a mesma tela.
* **Dinâmica:** As Brancas ficam na parte inferior. Após cada jogada, o turno alterna manualmente.
* **Regras:** O sistema valida todos os movimentos, impedindo jogadas ilegais.

### 2. 🤖 Jogar vs Computador (IA)
Desafie uma Inteligência Artificial básica embutida.
* **Dinâmica:** Você assume as Brancas. Após o seu movimento, a IA processa e executa a resposta das Pretas automaticamente em meio segundo.

### 3. 🌍 Multiplayer Online
Jogue contra qualquer pessoa através da internet com salvamento em nuvem via Firebase.
* **Criar Sala:** O criador joga sempre de **Brancas**.
* **Entrar em Sala:** O oponente joga de **Pretas** e o tabuleiro gira automaticamente para sua perspectiva.
* **Sincronização:** Movimentos atualizados em tempo real para ambos os jogadores.

---

## 🕹️ Controles e Interface

### Como Mover as Peças
A interação é feita por cliques simples, otimizada para Desktop e Mobile:
1.  **Selecionar:** Clique na peça desejada. O fundo ficará verde-oliva.
2.  **Visualizar:** Círculos translúcidos indicam casas para onde a peça pode ir.
3.  **Mover:** Clique na casa marcada ou na peça adversária para capturar.

### Painel de Status
Localizado acima do tabuleiro, informa:
* Vez do jogador (**Turno das Brancas/Pretas**).
* Alertas de **Xeque!** ou **Xeque-mate**.
* No modo online, confirma sua cor de atribuição.

---

## 🚀 Guia Técnico e Instalação

### Requisitos
* Navegador moderno (Chrome, Edge, Firefox ou Safari).
* Conexão com internet (apenas para o modo Multiplayer).

### Configuração do Firebase
Para habilitar o Multiplayer em seu próprio repositório:
1.  Crie um projeto no [Firebase Console](https://console.firebase.google.com/).
2.  Ative o **Cloud Firestore** e o **Anonymous Auth**.
3.  Substitua as credenciais no arquivo `js/firebase-config.js` (ou equivalente):

```javascript
const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "seu-projeto.firebaseapp.com",
  projectId: "seu-projeto",
  storageBucket: "seu-projeto.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc1234"
};
