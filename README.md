<img src="https://enterness.easychannel.online/assets/images/logo.png" alt="ENTERness Logo" width="200"/>

# 🧩 Desafio Técnico — Desenvolvedor FullStack (NestJS + React + TypeScript)

Olá, Desenvolvedor(a) 👋  
Bem-vindo(a) ao desafio técnico **Nível Hard** da **ENTERness**!

Este teste foi desenhado para avaliar não apenas sua capacidade de codificar, mas sua habilidade de arquitetar soluções **robustas, escaláveis e profissionais**. Queremos ver como você lida com persistência real, autenticação segura, concorrência em tempo real e uma UX impecável.

**Prazo sugerido:** 2 dias.  
**Foco:** Qualidade de código, Arquitetura (Clean/Hexagonal), Performance Frontend e "Refinamento" (detalhes que encantam).

---

## 🏛️ Cenário

Você deve construir um sistema de chat profissional onde o histórico é preservado, o acesso é seguro e a experiência do usuário é rica em feedback visual.
Nada de "em memória". Aqui, queremos ver **Banco de Dados Relacional** e **Regras de Negócio**.

---

## 🎯 Objetivo

Criar uma aplicação FullStack (Monorepo ou Repos separados) composta por:
1.  **Backend (API + WebSocket):** NestJS + MariaDB.
2.  **Frontend (SPA):** React + Vite + TailwindCSS.
3.  **Infra:** Docker & Docker Compose.

---

## 🔥 Requisitos Funcionais (Obrigatórios)

### 1. Autenticação & Usuários
- **Login/Cadastro:** O usuário deve criar conta (email/senha) ou entrar.
- **Segurança:** Autenticação via **JWT (JSON Web Token)**.
- **Socket Auth:** A conexão WebSocket só deve ser estabelecida se o token JWT for válido (Handshake Auth).

### 2. Gestão de Salas (Rooms)
- Usuários podem criar novas salas ou entrar em salas existentes.
- **Contador de Usuários:** A lista de salas deve mostrar, em tempo real, quantos usuários estão online naquela sala (Ex: "Devs Java (3 online)").
- **Relacionamento:** Um usuário pode estar em várias salas? Ou apenas uma por vez? (Defina a regra e implemente consistentemente). Sugestão: Apenas uma por vez para simplificar o socket, ou múltiplas para aumentar o desafio.

### 3. Mensagens & Persistência
- **Histórico:** Todas as mensagens devem ser salvas no **Banco de Dados (MariaDB)**.
- **Relacionamentos:**
    - `User` -> `Message` (1:N)
    - `Room` -> `Message` (1:N)
- Ao entrar em uma sala, o usuário deve carregar o histórico de mensagens anterior.

### 4. Funcionalidades de Chat (Real-time)
- Envio e recebimento de mensagens instantâneo.
- **Broadcast:** Apenas usuários na mesma sala recebem a mensagem.

---

## 💎 frontend Pro: Regras de Ouro (Aprofundado)

Aqui é onde avaliaremos sua senioridade no Front-end. Não basta funcionar, tem que ser **profissional**.

### 🎨 1. Arquitetura e State Management
- **Separação de Estado:** Demonstre clareza entre **Global State** (sessão do usuário, tema UI - ex: Zustand/Context API) e **Server State** (listas de mensagens, salas - ex: TanStack Query). Não misture tudo em um Redux gigante sem necessidade.
- **Feature-Based Structure:** Organize seu projeto por features (`features/auth`, `features/chat`), não apenas por tipo de arquivo (`components`, `hooks`).
- **Custom Hooks:** Toda lógica complexa deve ser extraída para hooks customizados (ex: `useChatSocket`, `useAuth`).

### ⚡ 2. Performance e UX Avançada
- **Optimistic Updates:** Quando o usuário enviar uma mensagem, ela deve aparecer **imediatamente** na lista (UI), antes mesmo do servidor confirmar (aplique status "enviando..." e trate erros caso falhe).
- **Lista Virtualizada:** Se o chat tiver 10.000 mensagens, o navegador vai travar? Implemente **Virtual Scroll** (ex: `react-virtuoso` ou `react-window`) para renderizar apenas o visível.
- **Skeleton Loading:** Nada de "spinners" genéricos o tempo todo. Use Skeletons enquanto os dados carregam.
- **Lazy Loading:** Use `React.lazy` e `Suspense` para carregar rotas ou componentes pesados sob demanda.

### 🛡️ 3. Robustez e Tratamento de Erros
- **Error Boundaries:** O que acontece se um componente quebrar? A tela fica branca? Implemente Error Boundaries para capturar falhas de renderização.
- **Reconexão Inteligente:** Se a internet cair, o chat deve avisar e tentar reconectar (Socket.io já ajuda, mas a UI deve refletir isso com clareza).
- **Tratamento de Forms:** Use **React Hook Form** + **Zod** para validação de formulários (Login/Cadastro). Feedback visual imediato nos inputs inválidos.

### ♿ 4. Acessibilidade (Bônus de Senioridade)
- A aplicação é navegável via **Teclado** (Tab)?
- Os inputs tem **Labels** corretos ou `aria-label`?
- O contraste de cores está adequado?

---

## ⚙️ Backend & DevOps (Requisitos Profissionais)

- **Banco de Dados:** Use **MariaDB** rodando via Docker.
- **ORM:** TypeORM (com Migrations).
- **Validação Robustas:** `class-validator` em todos os DTOs.
- **E2E & Testes Unitários:** O backend deve ter testes. Pelo menos os serviços principais.
- **Docker Compose:** O avaliador deve rodar apenas `docker-compose up` e ter **TUDO** rodando (Banco + Back + Front).

---

## 📊 Critérios de Avaliação Atualizados

| Critério | Peso | O que olhamos? |
| :--- | :--- | :--- |
| **Arquitetura (Front & Back)** | 30% | Separação de responsabilidades, File Structure, Clean Code. |
| **Frontend "Pro"** | 25% | Optimistic Updates, Virtualização, Gestão de Estado correta. |
| **Robustez & Bug-free** | 20% | O sistema aguenta refresh? O socket não duplica mensagens? |
| **Backend & Banco** | 15% | Modelagem, Migrations, Segurança. |
| **UI/UX & "Refinamento"** | 10% | Bonito, polido, animações fluídas. |

---

## 🚀 Entrega

1. Crie um repositório **público** no GitHub.
2. O `README.md` do projeto deve conter:
    - Instruções claras de como rodar (focadas no Docker).
    - Explicar **por que** escolheu tais bibliotecas no Frontend.
    - Prints ou GIF da aplicação rodando.
3. Envie o link para **jean@enterness.com** com o assunto "Desafio FullStack Senior - [Seu Nome]".

**Boa sorte! Surpreenda-nos.** 🚀

