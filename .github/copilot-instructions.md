# Instruções para o GitHub Copilot

## Sobre este projeto
- **Tipo:** API Backend em Node.js
- **Linguagem:** JavaScript (ES6+)
- **Runtime:** Node.js v20+

## Padrões de Código Obrigatórios

### Estilo de código
- Use `async/await` em vez de callbacks ou `.then()`
- Use `const` por padrão, `let` apenas quando reatribuição for necessária
- Nunca use `var`
- Use arrow functions para funções anônimas
- Use template literals para concatenação de strings

### Nomenclatura
- Variáveis e funções: `camelCase`
- Constantes globais: `UPPER_SNAKE_CASE`
- Arquivos: `kebab-case.js`
- Classes: `PascalCase`

### Estrutura de funções
- Funções devem ter no máximo 30 linhas
- Uma função deve fazer apenas uma coisa
- Sempre trate erros com try/catch em funções async

### Comentários
- Comente o "porquê", não o "o quê"
- Use JSDoc para funções públicas

## Exemplo de código que sigo

```javascript
/**
 * Busca um usuário pelo ID
 * @param {string} userId - ID do usuário
 * @returns {Promise<Object>} Dados do usuário
 */
const findUserById = async (userId) => {
  try {
    const user = await database.query('SELECT * FROM users WHERE id = ?', [userId]);
    
    if (!user) {
      throw new Error(`Usuário ${userId} não encontrado`);
    }
    
    return user;
  } catch (error) {
    console.error('Erro ao buscar usuário:', error.message);
    throw error;
  }
};
```

## Ao gerar código, sempre:
1. Adicione tratamento de erros
2. Valide parâmetros de entrada
3. Use nomes descritivos em português para variáveis de negócio
4. Adicione logs para debugging

## Ao explicar código:
- Assuma que entendo JavaScript avançado
- Explique conceitos de frameworks quando usados
- Dê contexto sobre "por que" uma abordagem é melhor
