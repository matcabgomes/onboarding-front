### Organização das pastas

## Nomes de arquivos

- Componente
    - Componente.js
    - Componente.style.js
    - Componente.utils.js
    - Componente.test.js
- Utils
    - nomeDaFuncao.js
    - outraFuncao.js

## Estrutura de arquivos básica
​
```bash
├── android* # Código fonte Android (*React-Native)
├── ios* # Código fonte iOS (*React-Native)
├── src # Código fonte JavaScript
│ 	├── assets # Imagens, fontes e assets no geral
│ 	│ 	└── images
│ 	├── components # Componentes genéricos da aplicação (style guide)
│ 	├── redux # Arquivos relacionados a store (redux)
│ 	│ 	├───configureStore.js # Arquivo de configuração da store
│ 	│ 	└───rootReducer.js # Root reducer da aplicação
│ 	├── utils # Utilitários gerais usados na aplicação inteira
│ 	│ 	├── colors.js
│ 	│ 	├── api.js
│ 	│ 	└── constants.js
│ 	├── screens # Pasta com as telas da aplicação
│ 	│ 	└── ScreenName # Exemplo de tela
│ 	│ 	    ├── ScreenName.js
│ 	│ 	    └── styles.js
│ 	├── hooks # Pasta contendo os hooks da aplicação (opcional)
│ 	└── App.js # Componente raiz da aplicação
├── README.md # Documentação básica sobre o projeto
├── package.json
├── .eslintrc.js # Arquivo de configuração do ESLint
├── .prettierrc # Arquivo de configuração do Prettier
├── index.js # Arquivo de entrada para registrar a aplicaçào
└── package.lock
```


## Atomic design
