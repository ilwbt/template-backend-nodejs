# Convenções do Projeto

## Estrutura de Arquivos

### Controllers
- Um arquivo por recurso: `users.controller.js`, `tasks.controller.js`
- Exporta um objeto com os métodos

```javascript
// src/controllers/users.controller.js
const usersService = require('../services/users.service');

const create = async (req, res) => {
  // ...
};

const findAll = async (req, res) => {
  // ...
};

module.exports = { create, findAll };
```

### Services
- Mesmo padrão dos controllers
- Nunca acessa `req` ou `res` diretamente
- Recebe dados puros, retorna dados puros

### Repositories
- Funções puras que interagem com o banco
- Nomeação: `createUser`, `findUserById`, `updateUser`, `deleteUser`

## Tratamento de Erros

Uso uma classe base para erros:

```javascript
// src/errors/AppError.js
class AppError extends Error {
  constructor(message, statusCode = 400) {
    super(message);
    this.statusCode = statusCode;
    this.isOperational = true;
  }
}

module.exports = AppError;
```

## Respostas da API

Formato padrão de sucesso:
```json
{
  "success": true,
  "data": { ... }
}
```

Formato padrão de erro:
```json
{
  "success": false,
  "error": {
    "message": "Descrição do erro",
    "code": "ERROR_CODE"
  }
}
```
