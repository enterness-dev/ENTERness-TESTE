<img src="https://enterness.easychannel.online/assets/images/logo.png" alt="ENTERness Logo" width="200"/>

# 🧩 Desafio Técnico — Desenvolvedor FullStack (NestJS + React + TypeScript)

Olá, Desenvolvedor 👋  
Bem-vindo(a) ao desafio técnico da **ENTERness**!

Este teste tem como objetivo avaliar sua capacidade de desenvolver uma aplicação **FullStack moderna**, aplicando **boas práticas de arquitetura**, **componentização**, **organização de código**, **uso de TypeScript**, e **integração em tempo real**.

Você terá **até 2 dias** para realizar o desafio a partir do recebimento deste documento.  
Mesmo que não finalize tudo, valorizamos muito **sua abordagem, clareza de código e estrutura do projeto**.

Se surgir qualquer dúvida, entre em contato pelo e-mail: **jean@enterness.com**  
Responderemos o mais rápido possível.

---

## 🎯 Objetivo do Projeto

Criar um **aplicativo de chat em tempo real** que permita a comunicação entre diferentes usuários (em múltiplas abas do navegador), demonstrando domínio em:

- **Back-end:** NestJS com TypeScript  
- **Front-end:** React com TypeScript  
- **Comunicação em tempo real:** WebSocket (Socket.IO, ws, ou outra lib equivalente)

---

## 🧠 Descrição do Desafio

Crie um chat web simples onde:

- Cada aba do navegador representa um usuário diferente.  
- Antes de acessar o chat, o usuário deve informar seu **nome de exibição**.  
- Após entrar, ele pode **enviar e receber mensagens** em tempo real.  
- Todas as abas conectadas devem receber as mensagens dos demais usuários.

---

## ⚙️ Requisitos Funcionais

1. **Login Simples**  
   - Solicitar o nome do usuário antes de acessar o chat.  
   - Armazenar o nome na sessão local (localStorage, context, etc.).  

2. **Chat em Tempo Real**  
   - Exibir mensagens enviadas por todos os usuários conectados.  
   - Mostrar o nome de quem enviou cada mensagem.  
   - Scroll automático para a última mensagem.

3. **Feedback Visual**  
   - Mostrar quando um usuário entra ou sai da sala.  
   - Mostrar mensagens de status (“Jean entrou na sala”, “Maria saiu da sala”, etc.).

---

## 🧩 Requisitos Técnicos (Obrigatórios)

### Backend
- **Framework:** NestJS (obrigatório)
- **Linguagem:** TypeScript
- **Comunicação:** WebSocket (ex: Socket.IO)
- **Persistência:** Em memória (não é necessário banco)
- **Boas práticas:** uso de módulos, serviços, DTOs e tipagem forte.

### Frontend
- **Framework:** React com TypeScript
- **Gerenciamento de estado:** useContext, Zustand, Redux Toolkit ou outro equivalente
- **Componentização:** componentes reaproveitáveis e bem estruturados
- **Comunicação com backend:** via WebSocket
- **UI mínima:** campo de mensagem, botão enviar e lista de mensagens

---

## 💎 Diferenciais (Bônus)

Esses itens não são obrigatórios, mas **valem pontos extras** e mostram seu domínio técnico:

### 👨‍💻 Backend
- Implementar **salas de chat** (usuário escolhe ou cria uma sala antes de entrar)
- Adicionar **validação** usando `class-validator`
- Criar **serviço de logging** customizado
- Estrutura modular limpa (Domain Driven Design, Clean Architecture)

### 💅 Frontend
- Layout **responsivo e intuitivo**
- Animações sutis e feedbacks visuais (ex: envio de mensagem, entrada/saída)
- Suporte a **emojis** ou upload de **imagens**
- Testes unitários simples (ex: Jest, React Testing Library)

### 🚀 DevOps / Infra
- Configuração via **Docker** (opcional)
- Script `npm run build` funcional para front e back
- Configuração de `.env` e variáveis de ambiente
- Documentação de setup (`README.md` com instruções de execução)

---

## 🧭 Critérios de Avaliação

| Critério | Peso | Descrição |
|-----------|------|-----------|
| **Clareza e Organização do Código** | 25% | Estrutura limpa, coesa e fácil de entender |
| **Boas Práticas e Arquitetura** | 20% | Uso adequado de módulos, tipagem e separação de responsabilidades |
| **Funcionalidade** | 20% | O chat funciona em tempo real conforme o esperado |
| **Componentização / Reutilização** | 15% | Código React modular e reaproveitável |
| **UX e Design** | 10% | Interface simples, agradável e funcional |
| **Extras e Criatividade** | 10% | Diferenciais técnicos e melhorias implementadas |

---

## 🧾 Entrega

Envie o projeto por meio de um **repositório público no GitHub**, contendo:

- Código-fonte completo (front e back)  
- Instruções de execução no arquivo `README.md`  
- (Opcional) Link de deploy se desejar publicar (ex: Render, Vercel, etc.)

---

## 💬 Observações Finais

- Foque na **qualidade e clareza do código**, não apenas na entrega funcional.  
- Demonstre boas práticas e preocupação com manutenção.  
- Todos os participantes recebem **feedback construtivo**.  

Boa sorte e bom código! 🚀  
**Equipe ENTERness**

