### Análise estática de código

## Prettier
​
O Prettier é um formatador que reescreve todo o código do zero seguindo uma série de regras e garantindo um padrão de estilo. A ferramenta torna o código mais legível e facilita o trabalho de diversos desenvolvedores de um mesmo projeto.
​
[`Sobre o Prettier e Documentção`](https://prettier.io/docs/en/index.html)
​
- Instalação
​
1. No VSCode ir na área de extensões, procurar por Prettier e instalá-la.
2. No arquivo de configuração do VSCode inserir:
​
```json
{
  ...
  "[javascript]": {
    "editor.formatOnSave": true
  },
  ...
}
```
​
- Configuração:
​
1. Caso não exista, criar um arquivo com o nome _.prettierrc_ na raiz do projeto (versões do React Native > 0.61.0 criam este arquivo automaticamente em novos projetos)
​
2. O arquivo deve conter o seguinte código:
​
```json
{
  "arrowParens": "avoid",
  "bracketSpacing": true,
  "htmlWhitespaceSensitivity": "css",
  "insertPragma": false,
  "jsxBracketSameLine": false,
  "jsxSingleQuote": true,
  "proseWrap": "always",
  "quoteProps": "as-needed",
  "requirePragma": false,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "none",
  "useTabs": false,
  "printWidth": 80
}
```
​
Para maiores dúvidas e/ou informações, contate o líder técnico
​
---
​
## ESLint
​
O ESLint é uma ferramenta utilizada para fazer análises estatísticas de código buscando trechos que não condizem com padrões de boas práticas. Ele facilita a descoberta de erros além de manter o código limpo e organizado de maneira fácil e prática.
​
[`Sobre o ESLint e Documentção`](https://eslint.org/docs/)
​
Nós possuímos um padrão base do ESLint que deve ser implementado em todos os projetos. Caso necessário, os desenvolvedores responsáveis por cada projeto têm liberdade para implementar novas regras, **_desde que sejam mantidas as regras base_**.
​
- Instalação:
​
1. No VSCode ir na área de extensões, procurar por ESLint e instalá-la.
2. Na linha de comando executar: _yarn add eslint -D_
​
Nossas regras do ESLint utilizam algumas bibliotecas com definições de regras que devem ser instaladas via linha de comando:
​
3. [`eslint-config-airbnb`](https://www.npmjs.com/package/eslint-config-airbnb):
   _yarn add eslint-config-airbnb -D_
4. [`eslint-config-prettier`](https://github.com/prettier/eslint-config-prettier):
   _yarn add eslint-config-prettier -D_
5. [`eslint-plugin-prettier`](https://github.com/prettier/eslint-plugin-prettier):
   _yarn add eslint-config-airbnb -D_
6. [`eslint-plugin-react`](https://github.com/yannickcr/eslint-plugin-react):
   _yarn add eslint-plugin-react -D_
7. [`eslint-plugin-react-hooks`](https://www.npmjs.com/package/eslint-plugin-react-hooks):
   _yarn add eslint-plugin-react-hooks -D_
8. [`eslint-plugin-import`](https://github.com/benmosher/eslint-plugin-import):
   _yarn add eslint-plugin-import -D_
​
- Configuração:
​
1. Caso não exista, criar um arquivo com o nome _.eslintrc.js_ na raiz do projeto (versões do React Native > 0.61.0 criam este arquivo automaticamente em novos projetos)
​
2. O arquivo deve conter o seguinte código:
​
```javascript
module.exports = {
  extends: ["airbnb", "plugin:prettier/recommended", "prettier/react"],
  plugins: ["react", "prettier", "react-hooks"],
  globals: {
    __DEV__: true,
    fetch: false
  },
  env: {
    jest: true
  },
  rules: {
    "comma-dangle": "off",
    "react/jsx-filename-extension": [1, { extensions: [".js", ".jsx"] }],
    "import/prefer-default-export": "off",
    "react/jsx-one-expression-per-line": "off",
    "react/prop-types": ["error", { ignore: ["navigation"] }],
    "react/state-in-constructor": "off",
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exhaustive-deps": "warn"
  }
};
```
​
---
