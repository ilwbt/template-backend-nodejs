# Arquitetura do Projeto

## Visão Geral
[Descreva em 2-3 frases o que o projeto faz]

## Estrutura de Pastas

```
src/
├── index.js           # Ponto de entrada da aplicação
├── config/            # Configurações (banco, variáveis de ambiente)
├── routes/            # Definição das rotas/endpoints
├── controllers/       # Lógica de requisição/resposta HTTP
├── services/          # Regras de negócio
├── repositories/      # Acesso ao banco de dados
├── middlewares/       # Funções intermediárias (auth, validação)
├── utils/             # Funções auxiliares reutilizáveis
└── errors/            # Classes de erro customizadas
```

## Fluxo de uma Requisição

```
Request → Route → Middleware → Controller → Service → Repository → Database
                                    ↓
Response ← Controller ← Service ←──┘
```

### Explicação do fluxo:
1. **Route:** Define qual função vai tratar a URL
2. **Middleware:** Valida token, formata dados, etc.
3. **Controller:** Recebe a requisição, chama o service, retorna resposta
4. **Service:** Contém a lógica de negócio (as regras do sistema)
5. **Repository:** Faz queries no banco de dados

## Banco de Dados
- **Tipo:** [SQLite/PostgreSQL/MongoDB/etc]
- **ORM/Driver:** [Nenhum/Knex/Prisma/etc]

## Dependências Principais
| Pacote | Versão | Propósito |
|--------|--------|-----------|
| ... | ... | ... |
