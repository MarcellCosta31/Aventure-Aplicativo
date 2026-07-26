<div align="center">

# Aventure

### Transforme sua vida em uma aventura épica

Um aplicativo mobile que gamifica produtividade, estudos e treinos usando mecânicas de RPG.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![React Native](https://img.shields.io/badge/React%20Native-0.81-blue.svg)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-54-purple.svg)](https://expo.dev/)

</div>

---

## Visão Geral

O **Aventure** é um aplicativo mobile desenvolvido em React Native com Expo que transforma suas atividades diárias em uma experiência de RPG. Crie seu herói, complete tarefas, estude e treine para subir de nível, desbloquear classes e conquistar emblemas — tudo enquanto melhora sua produtividade de verdade.

## Funcionalidades

###  Criação de Personagem
- Crie seu herói personalizado com nome e avatar
- Avatar pixel art editável diretamente no app
- Sistema de atributos: Mente, Corpo, Espírito e Determinação

###  Sistema de Progressão
- Ganhe XP ao completar tarefas e anotações
- Suba de nível com distribuição automática de pontos
- HP que varia conforme seu nível (e pode chegar a zero!)
- Sistema de streak diário para manter a consistência

###  Sistema de Classes
- Suas atributos determinam sua classe (arquétipo do herói)
- Classes evoluem conforme você distribui pontos

###  Emblemas e Conquistas
- Emblemas desbloqueados conforme seu nível
- Barra de progresso mostrando quanto falta para o próximo emblema

###  Sistema de Tarefas
- Crie tarefas com XP, atributo-alvo e penalidade de HP
- Suporte a tarefas recorrentes (diárias, semanais)
- Prazos com penalidade por atraso (perda de HP e Determinação)
- **Modo Foco**: timer Pomodoro integrado para tarefas com duração

###  Sistema de Estudos
- Crie pastas de estudos organizadas por cor
- Adicione anotações dentro de cada pasta
- Sistema de revisões periódicas

###  Sistema de Treinos
- Crie treinos personalizados com exercícios
- Execute treinos com contagem de séries e repetições
- Ganhe XP e atributos ao completar treinos

###  Notificações
- Notificações personalizadas para lembretes
- Sons de notificação customizados

###  Modo Offline
- Funciona sem conexão com a internet
- Sincronização automática quando voltar online
- Dados armazenados localmente com AsyncStorage

## Capturas de Tela

<div align="center">

![Home](https://via.placeholder.com/300x600/0f172a/facc15?text=Aventure+Home)
![Tarefas](https://via.placeholder.com/300x600/0f172a/facc15?text=Tarefas)
![Estudos](https://via.placeholder.com/300x600/0f172a/facc15?text=Estudos)

</div>

## Tecnologias Utilizadas

| Tecnologia | Versão | Uso |
|---|---|---|
| React Native | 0.81 | Framework mobile |
| Expo | 54 | Plataforma de desenvolvimento |
| Firebase | 12.12 | Backend (Auth + Firestore) |
| TypeScript | 5.9 | Tipagem estática |
| React Navigation | 7.x | Navegação entre telas |
| AsyncStorage | 2.2 | Armazenamento local |
| Expo Notifications | 0.32 | Notificações push |
| Expo Image Picker | 17.0 | Seleção de imagens |

## Estrutura do Projeto

```
Aventure/
├── App.tsx                    # Ponto de entrada e configuração de navegação
├── firebase.ts                # Configuração do Firebase
├── index.ts                   # Registro do app
├── assets/                    # Ícones, sons e imagens
├── components/                # Componentes reutilizáveis
│   ├── ConnectionStatus.tsx   # Indicador de status da conexão
│   ├── FocusTimerModal.tsx    # Modal do timer Pomodoro
│   ├── PixelArtEditor.tsx     # Editor de pixel art para avatar
│   └── PixelArtView.tsx       # Visualizador de pixel art
├── data/                      # Dados estáticos
│   └── palavrasAtributos.json # Palavras para distribuição de atributos
├── hooks/                     # Custom hooks
│   ├── useFocusTimer.ts       # Lógica do timer de foco
│   └── useIsDead.ts           # Verificação de HP zerado
├── screens/                   # Telas do aplicativo
│   ├── AuthScreen.tsx         # Login/Cadastro
│   ├── CreateCharacterScreen.tsx # Criação de personagem
│   ├── HomeScreen.tsx         # Tela principal (Dashboard)
│   ├── TarefasScreen.tsx      # Lista de tarefas
│   ├── CriarTarefaScreen.tsx  # Criação de tarefa
│   ├── EstudosScreen.tsx      # Pastas de estudos
│   ├── PastaAnotacoesScreen.tsx # Anotações dentro da pasta
│   ├── CriarAnotacaoScreen.tsx # Criação de anotação
│   ├── RevisaoScreen.tsx      # Sistema de revisões
│   ├── TreinosScreen.tsx      # Lista de treinos
│   ├── CriarTreinoScreen.tsx  # Criação/edição de treino
│   ├── ExecutarTreinoScreen.tsx # Execução de treino
│   ├── PersonagemScreen.tsx   # Perfil do personagem
│   ├── ConfiguracoesScreen.tsx # Configurações
│   └── SobreCriadorScreen.tsx # Sobre o criador
├── services/                  # Serviços de negócio
│   ├── authService.ts         # Autenticação e sessão
│   ├── studyService.ts        # CRUD de pastas e anotações
│   ├── trainingService.ts     # CRUD de treinos e exercícios
│   ├── notificationService.ts # Notificações push
│   ├── offlineService.ts      # Modo offline e sincronização
│   ├── classSystem.ts         # Sistema de classes e emblemas
│   ├── characterService.ts    # Serviço de personagem
│   ├── taskRecurrenceService.ts # Recorrência de tarefas
│   ├── wordListService.ts     # Serviço de palavras
│   ├── aiService.ts           # Serviço de IA
│   └── localClassifier.ts     # Classificador local
├── src/
│   ├── constants/classes.ts   # Constantes de classes
│   └── services/classService.ts # Serviço de cálculo de classe
└── utils/                     # Utilitários gerais
```

## Pré-requisitos

- [Node.js](https://nodejs.org/) (v18 ou superior)
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- [Firebase](https://console.firebase.google.com/) (conta para configurar o backend)

## Instalação

1. **Clone o repositório:**

```bash
git clone https://github.com/SEU_USERNAME/Aventure.git
cd Aventure
```

2. **Instale as dependências:**

```bash
npm install
```

3. **Configure o Firebase:**

Crie um projeto no [Firebase Console](https://console.firebase.google.com/) e substitua as credenciais no arquivo `firebase.ts`:

```typescript
const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "SEU_AUTH_DOMAIN",
  projectId: "SEU_PROJECT_ID",
  storageBucket: "SEU_STORAGE_BUCKET",
  messagingSenderId: "SEU_SENDER_ID",
  appId: "SEU_APP_ID"
};
```

4. **Execute o app:**

```bash
# Expo
npx expo start

# Android
npx expo run:android

# iOS
npx expo run:ios
```

## Como Jogar

1. **Crie seu herói** — Escolha um nome e personalize seu avatar
2. **Complete tarefas** — Ganhe XP e distribua pontos nos atributos
3. **Estude** — Crie pastas de anotações e faça revisões
4. **Treine** — Monte rotinas de exercícios e execute
5. **Suba de nível** — Desbloqueie novas classes e emblemas
6. **Mantenha a sequência** — Não deixe seu HP chegar a zero!

## Mecânicas do Jogo

| Ação | Recompensa |
|---|---|
| Completar tarefa | +XP, +1 EXP no atributo, +0.5 Determinação |
| Criar anotação | +XP, +1 EXP Mente |
| Executar treino | +XP, +1 EXP no atributo escolhido |
| Streak diário | Bônus de XP |
| Tarefa atrasada | -HP, -1 Determinação |
| HP = 0 | Personagem "derrotado" — sem criar pastas/treinos |

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

<div align="center">

Feito com dedicação por **Marcell Costa**

</div>
