# Template Backend Node.js

> Template de projeto backend Node.js otimizado para GitHub Copilot

## 📋 Sobre

Este é um template para projetos backend em Node.js, estruturado para trabalhar de forma otimizada com GitHub Copilot (Chat, Code Completion e Coding Agent).

## 🚀 Começando

### Pré-requisitos
- Node.js v20+
- npm ou yarn

### Instalação

```bash
# Clone o repositório (ou use como template)
git clone https://github.com/ilwbt/template-backend-nodejs.git

# Entre na pasta
cd template-backend-nodejs

# Instale as dependências
npm install

# Configure as variáveis de ambiente
cp .env.example .env

# Rode o projeto
npm run dev
```

## 📁 Estrutura do Projeto

```
├── .github/
│   └── copilot-instructions.md  # Instruções para o GitHub Copilot
├── docs/
│   ├── ARCHITECTURE.md          # Arquitetura do projeto
│   ├── CONVENTIONS.md           # Convenções de código
│   ├── tasks/                   # Gestão de tarefas
│   │   ├── current.md           # Tarefas em andamento
│   │   ├── backlog.md           # Backlog
│   │   └── completed/           # Histórico
│   └── specs/                   # Especificações de features
├── src/                         # Código fonte
├── package.json
└── README.md
```

## 🤖 Usando com GitHub Copilot

Este projeto está configurado para funcionar de forma otimizada com o GitHub Copilot:

1. **Copilot Chat:** Referencie arquivos em `docs/` para contexto
2. **Copilot Coding Agent:** Use specs em `docs/specs/` para gerar PRs
3. **Code Completion:** As instruções em `.github/copilot-instructions.md` são aplicadas automaticamente

### Exemplos de prompts úteis

**Para planejamento:**
> "Leia docs/tasks/current.md e me ajude a quebrar a tarefa em subtarefas menores"

**Para gerar código:**
> "Seguindo as convenções em docs/CONVENTIONS.md, crie o service de autenticação"

**Para o Coding Agent:**
> "Crie um PR implementando a spec em docs/specs/nome-da-feature.md"

## 📝 Licença

Este projeto está sob a licença MIT.
