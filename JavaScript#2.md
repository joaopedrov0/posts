## No post anterior
Anteriormente, eu expliquei um pouco sobre JavaScript, por que escolhi ele e como criar o famoso "Hello World", agora vou explicar um pouco sobre variáveis.

## Conceito
Variáveis são um conceito fundamental em programação, se tratam de blocos de informações que você pode guardar coisas neles para usar mais tarde ou até mesmo trocar o que está guardado por outra coisa, caso necessário.

## Declarando uma variável
A declaração de variáveis em JavaScript pode ser feita usando uma de três opções de palavras-chave, "`let`", "`var`" ou "`const`"

### Nomeando a variável
Depois da palavra chave, você deve escrever o nome que você quer dar para essa variável, esse nome **não pode começar com um número** e **não deve conter caracteres especiais**, com raras exceções, como _underline_ "`_`".

### Atribuindo um valor à variável
Normalmente, a atribuição de um valor à uma variável é feita juntamente de sua declaração, apesar de isso não ser obrigatório.
Para isso, você deve usar o operador de atribuição `=` dessa forma:

```javascript
var texto = "Hello World"
```

> No exemplo acima eu usei `var` para declarar a variável, mas nesse caso eu poderia usar tanto `var`, quanto `let` ou até mesmo `const`

#### Mas o que está acontecendo?
No exemplo acima, declaramos uma variável chamada `texto` usando a palavra-chave `var` e, em seguida, guardamos dentro dela um texto, `"Hello World"`.

## Exibindo o valor da variável
Lembra do exemplo do post anterior? Nós usamos o método `console.log()` para exibir uma mensagem na tela.
Tente combinar as duas coisas, experimente colocar a variável dentro do `console.log()` (dentro das aspas).

```javascript
var texto = "Hello World"
console.log(texto) // Vai exibir o conteúdo da variável "texto"
```

## Diferença entre `const`, `let` e `var`
Eu disse anteriormente que você poderia usar qualquer uma dessas para declarar uma variável, e realmente pode, porém, ela vai se comportar de forma diferente em alguns casos dependendo da palavra-chave que você usar.

### `let` e `var`
Essas duas palavras-chave podem ser usadas para criar variáveis que poderão ser sobrescritas futuramente, isso significa que se você definir que a variável vai receber um valor, e depois dizer que ele vai valer outro valor, isso é possível, observe o exemplo abaixo:
```javascript
let mensagem = "Primeira mensagem"
console.log(mensagem) // "Primeira mensagem"
mensagem = "Segunda mensagem"
console.log(mensagem) // "Segunda mensagem"
```
O mesmo vale para `var`
```javascript
var mensagem = "Primeira mensagem"
console.log(mensagem) // "Primeira mensagem"
mensagem = "Segunda mensagem"
console.log(mensagem) // "Segunda mensagem"
```
A diferença entre `let` e `var` é algo um pouco mais específico e que eu não vou abordar agora no começo pois não julgo necessário para quem está começando, porém, nada me impede de explicar a diferença futuramente.

### `const`
A palavra-chave `const` é um pouco diferente, esse termo "const" se refere a "constante", o que significa que ela não pode ser sobrescrita, uma vez que você atribuir um valor pra ela, ela ficará com aquele valor até o fim.
Observe o mesmo exemplo anterior, porém agora usando `const`:
```javascript
const mensagem = "Primeira mensagem"
console.log(mensagem) // "Primeira mensagem"
mensagem = "Segunda mensagem" // Uncaught TypeError: Assignment to constant variable. 
console.log(mensagem) // Código não executado
```
Observe que o código parou na terceira linha, com uma mensagem de erro. Isso acontece porque eu defini que a variável `mensagem` seria uma constante, porém, eu tentei escrever um novo valor nela na linha 3, exatamente na linha que gerou a mensagem de erro.

## Extra: Comentários
É possível deixar marcações no código que não serão interpretadas como código pelo computador, essas marcações são chamadas de "Comentários".

### Comentário de uma linha
É possível comentar uma linha adicionando duas barras (//) no início do comentário.

```javascript
// Comentário
var mensagem = "Hello World" // Comentário
```

### Comentário de múltiplas linhas
Para comentar múltiplas linhas em JavaScript, basta colocar o comentário entre uma barra e um asterisco, como o exemplo abaixo

```javascript
/* Comentário */

/*
Comentário
Outro comentário
*/
```

## Deixe seu feedback!
Tem algum comentário, dúvida ou sugestão sobre o post? Sinta-se a vontade para usar os comentários para isso! Responderei assim que possível.
