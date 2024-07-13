## O que são operadores?
Operadores são símbolos usados para fazer algumas coisas com os dados das variáveis. Com operadores é possível por exemplo, fazer somas, comparações, atribuições, e muito mais.

## Por que são importantes?
Os operadores fazem parte da etapa mencionada no post anterior de "processar os dados", parte essencial de qualquer algoritmo.

## Tipos de operadores
Existem vários tipos de operadores que cumprem diferentes funções, vou explicar alguns deles a seguir.

### Operadores aritméticos
Os operadores aritméticos são usados para fazer operações matemáticas, como somas, subtrações, multiplicações, etc.
Observe alguns deles e em seguida alguns exemplos

- Soma: `+`
- Subtração: `-`
- Multiplicação: `*`
- Divisão: `/`
- Resto da divisão: `%`
- Potência: `**`

> Diferente de algumas linguagens, o JavaScript tem um operador que é capaz de fazer operações de potenciação nativamente.

```javascript
console.log(2 + 3) // 5
sumTest = 3 + 4 // Atribuir o resultado de uma operação à uma variável
console.log(sumTest) // 7

console.log(sumTest - 5) // 2

console.log(2 * 3) // 6

console.log(10 / 2) // 5

// Resto da divisão é o que sobraria de uma divisão inteira.
// Por exemplo, 10 / 3 = 3.3333...
// Nesse caso, a divisão inteira seria apenas 3
// Porém 3 * 3 resulta em 9 e não em 10, esse 1 que falta é o resto da divisão

console.log(10 % 3) // 1

console.log(2**4) // 16
// 2**4 é equivalente a 2⁴
```

### Operadores de atribuição
Os operadores de atribuição servem para interagir com a forma de atribuir valores à variáveis. O mais simples deles é o `=`, que já usamos diversas vezes anteriormente. Porém, é possível combinar o operador de atribuição com operadores aritméticos para fazer novas atribuições a valores que já tem uma variável, observe o exemplo abaixo:
```javascript
num = 3
num += 4 // Ele está pegando o valor de "num", somando 4 e atribuindo o resultado à "num" novamente
console.log(num) // 7

num *= 2
console.log(num) // 14

num /= 7
console.log(num) // 2
```

Aqui está uma lista de alguns dos operadores de atribuição que podem ser usados:
- `+=`
- `-=`
- `*=`
- `/=`
- `%=`
- `**=`

### Operadores de incremento
Operadores de incremento são semelhantes aos operadores de atribuição combinado com operadores aritméticos, porém, eles são mais simples servem apenas com soma e subtração, e apenas de um em um. Para usar um operador de incremento, basta acrescentar `++` (incremento) ou `--` (decremento) na frente do nome da variável.
```javascript
num = 3
console.log(num) // 3
num++
console.log(num) // 4
num++
num++
console.log(num) // 6
num--
console.log(num) // 5
```

### Operadores relacionais
Os operadores relacionais são usados para comparar (relacionar) dois valores da forma desejada e, por fim, devolvem um valor booleano.
- Maior: `>`
- Menor: `<`
- Maior ou igual: `>=`
- Menor ou igual: `<=`
- Igual: `==`
- Diferente: `!=`
- Igualdade restrita: `===`
- Diferença restrita `!==`

Observe alguns exemplos:
```javascript
console.log(2 > 3) // Retorna "false"
console.log(2 < 3) // Retorna "true"
console.log(3 > 3) // Retorna "false"
console.log(3 >= 3) // Retorna "true"
console.log(3 != 4) // Retorna "true"
console.log(3 != 3) // Retorna "false"
console.log(3 != "3") // Retorna "false"
console.log(3 !== "3") // Retorna "true"
console.log(3 === "3") // Retorna "false"

// Nesses últimos 2 exemplos eu usei a diferença e igualdade 
// restritas, para demonstrar que a igualdade e diferença simples 
// "releva" o fato de o tipo da variável é diferente e leva
// em consideração o conteúdo. Enquanto a diferença e
// igualdade restrita levam o tipo do valor em consideração.
```

> Atenção, o "igual" como operador relacional (`==`) é diferente do "igual" como operador de atribuição (`=`)

### Operadores lógicos
Os operadores lógicos são usados para relacionar valores usados em operadores relacionais. Alguns desses operadores são o **and**, o **or** e o **not**, representando respectivamente, **conjunção**, **disjunção** e **negação**.
Os operadores lógicos interagem com **valores booleanos**, e como mencionado anteriormente, operadores relacionais retornam valores booleanos, por isso eles funcionam bem juntos.

- Negação: `!`
- Conjunção: `&&`
- Disjunção: `||`

#### Negação
O operador lógico de negação (not) inverte o valor booleano de um valor, transformando "true" em "false" e vice-versa.

> !p = "Não p"

#### Conjunção
O operador lógico de conjunção (and) devolve `true` se ambas as proposições são verdadeiras e `false` em qualquer outra situação

> p && q = "p e q"

#### Disjunção
O operador lógico de disjunção (or) devolve `true` se um dos valores for verdadeiro ou se ambos forem. Devolve `false` caso ambos forem falsos.

> p || q = "p ou q"

```javascript
console.log(!true) // Retorna "false"
console.log(!false) // Retorna "true"
console.log(true && true) // Retorna "true"
console.log(true && false) // Retorna "false"
console.log(false && true) // Retorna "false"
console.log(false && false) // Retorna "false"
console.log(true || true) // Retorna "true"
console.log(true || false) // Retorna "true"
console.log(false || true) // Retorna "true"
console.log(false || false) // Retorna "false"
```

## Um conselho
A partir daqui, eu recomendo que você comece a se perguntar coisas sobre os assuntos que está aprendendo e, não apenas analisar os exemplos que eu deixo aqui, como também ir atrás de fazer seus próprios testes, buscando suas próprias respostas pra suas perguntas! Teste tudo que quiser, seja curioso(a).

## Deixe seu feedback!
Espero que tenham entendido e caso tenham alguma dúvida, sugestão ou correção, não deixem de colocar nos comentários, responderei assim que possível.