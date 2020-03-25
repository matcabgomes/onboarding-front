### Base
- Segmente o código usando espaços que façam sentido.
- Segmente o código de teste no modelo AAA (Arrange, Act, Assert)

### Funcional Components X Class Components

Na [documentação oficial do React](https://pt-br.reactjs.org/), uma das primeiras informações que temos é que ele é uma biblioteca **declarativa**. Atualmente no padrão de classes utilizamos uma linguagem mais imperativa, ou seja, nós descrevemos como será o comportamento ou descrevemos **COMO**. Com a nova API de hooks do React podemos escrever então de forma mais declarativa que seria baseado no comportamento, ou seja, nós apenas descrevemos **O QUE** vamos fazer se algum comportamento ocorrer.

Evidentemente usamos as duas formas durante a escrita do código, mas falando de um componente do React em si usando a API de Hooks fica muito mais evidente essa forma declarativa. De acordo com o [blog da Rocketseat](https://blog.rocketseat.com.br/react-hooks/) Hooks trazem menos verbosidade ao código e melhoram o isolamento de responsabilidades. A equipe do React [nem diz que deve nem que não deve](https://pt-br.reactjs.org/docs/hooks-faq.html#should-i-use-hooks-classes-or-a-mix-of-both) usar Funcional Components ou Hooks ao invés de classes, mas poderia ser uma boa prática utilizar.

- A partir de hoje, tudo que for criado é com Hooks (salve exceções com código que não se encaixa bem com o Redux House)
- O que for legado com Classe manter na Classe

### Nome de componentes e funções

Precisam fazer sentido com o que será executado. Os nomes precisam ser claros e sem ambiguidade indicando o que a função faz.
Exemplo:
Formulário de **Cadastrar Usuário** pode ser chamada de **CreateUserForm**.
```javascript
// Função construtora ou um Componente
export function CreateUserForm() {
    ...
}
```
Funções não-construtoras ou que não são componentes, vamos usar o padrão camelCase
Alguns exemplos de funções:
```javascript
    isFormValid(): Boolean {
        ...
    }
    
    hasEmail (): Boolean {
        ...
    }
    const getAddress = () => {}
    const setName = name => {}
```
Os parâmetros da função também precisam fazer sentido:
```javascript
function getPhone = x => { ... } // não legal
function getPhone = phone => { ... } // legal
```

- Escolha nomes que façam sentido com a segmentação das telas. Use Inglês para manter o padrão.
- Use verbos como a primeira palavra das funções 

### Nome de variáveis

Nomes de variáveis devem dizer o que ela faz, porque existe e como usar, precisam estar no padrão camelCase ou em UpperCase quando forem constantes.
```javascript
const FIREBASE_KEY = 1001110111;
const liveStatus = {
    LIVE: 'live',
    UNPUBLISHED: 'unplublished'
}
for(let key in obj) {...}
```
Mais exemplos:
```javascript
let h = 0; // horas --> Não legal
let hour = 0; // Legal
```

- Escolha nomes que façam sentido. Use inglês para manter o padrão.
- Booleanos use is ou has