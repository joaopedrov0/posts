## O que são Tipos de Variáveis?
No post anterior, expliquei sobre o conceito de variáveis.
Lembra o conceito de guardar informações? É essencial ter em mente que você vai trabalhar com a **entrada** de dados que serão **processados** e, posteriormente, resultarão em uma **saída**.
Esses conceitos de entrada, processamento e saída são essenciais na programação e posso abordar futuramente em um outro post com um pouco mais de aprofundamento.
Mas por agora, o que você precisa saber é que esse **processamento** envolve o que você quer **fazer** com esses dados para conseguir o resultado desejado. Por exemplo, vamos supor que você queira um programa que receba duas variáveis e some elas, devolvendo o resultado. Se você inserir 2 e 3, o resultado esperado é 5, certo? Mas o que você acha que acontece se inserir "dois" e "três" como valores de entrada? Você precisa saber o tipo de dado que você está lidando para que tudo ocorra como o planejado, isso vai ficar mais claro com o tempo.

## Quais são os tipos de variáveis?
O JavaScript tem três tipos **primitivos** de variáveis, que são os tipos mais básicos de variáveis, são eles **String**, **Number** e **Boolean**.

### String
Strings são um tipo de variável usado para guardar texto, cadeias de caracteres. Normalmente strings são demarcadas por aspas simples ou duplas, ou crase, possibilitando o uso de **template strings**, mas isso não é assunto pra agora.

### Number
De modo bem intuitivo, variáveis do tipo Number guardam números, que podem ser o que chamamos de **inteiro** ou **float**.

#### Inteiro (Integer ou int)
Números inteiros são, da mesma forma que na matemática, números que vão desde o infinito negativo até o infinito positivo, sem casas decimais.

#### Ponto Flutuante (Float)
Nós chamamos de Float, ou número com **ponto flutuante** números com casas decimais, ainda que nulas (igual a 0).

> O nome "Ponto Flutuante" se refere ao modo que essas variáveis são guardadas no binário do computador, posso fazer um post sobre esse assunto futuramente.

### Boolean
Variáveis do tipo Boolean guardam apenas dois valores, verdadeiro ou falso.

> O termo "Boolean" ou "Booleano" se refere a **George Boole**, criador da álgebra booleana que futuramente foi essencial para o avanço da computação. Essa forma "nova" de fazer contas se baseia apenas na existência de proposições **verdadeiras** ou **falsas**.

### `undefined`
Esse tipo é algo bem específico e não acho necessário você tentar entender por agora, mas quero que você saiba que ele existe. "undefined" é usado para se referir a valores "não definidos". Por exemplo, se você declarar uma variável mas não atribuir nenhum valor à ela, como eu disse no post anterior que é possível fazer, caso tente exibir ela, "undefined" será exibido no lugar uma vez que você não atribuiu nenhum valor àquela variável.

```javascript
var exemplo
console.log(exemplo) // undefined
```

### Function e Object
Esses não são tipos primitivos do JavaScript, pois não são usados para guardar variáveis **simples**, mas sim estruturas mais complexas como **objetos**, **arrays** e **funções**, como veremos futuramente.

## Como definir o tipo da variável?
O JavaScript é uma linguagem de **tipagem dinâmica fraca**, vou explicar brevemente o que isso significa.

### "Tipagem"
O estilo de tipagem é algo que pode variar de linguagem pra linguagem e ele diz como a que você está trabalhando lida com tipagem, podendo ela variar entre **estática** e **dinâmica**, assim como podem ser **fortemente** tipadas ou **fracamente** tipadas.

### "Dinâmica"
A tipificação **dinâmica** permite que o tipo da variável seja alterado depois da variável ser declarada. Além disso, não é necessário que o programador defina o tipo da variável na sua declaração, a própria linguagem é capaz de fazer isso.

### "Fraca"
A tipagem **fraca** permite que sejam feitas operações entre tipos diferentes sem que o programador converta a linguagem de um tipo para outro, desde que isso seja ao menos possível.

### Resumindo
No JavaScript você não precisa fazer esse processo de dizer o tipo da variável, uma vez que, vendo o valor armazenado na variável, o JavaScript é capaz de dizer qual o tipo adequado para essa variável.

```javascript
var exemploNumero = 34 // Number integer
var exemploTexto = "Trinta e quatro ☕" // String
var exemploBooleano = true // Boolean
```

## Como saber o tipo de uma variável?
Para finalizar, já que o JavaScript não requer que fique explícito o tipo de uma variável, vou apresentar uma forma de você descobrir isso.

### Função `typeof()`
A função `typeof()` **recebe** uma variável (dentro dos parênteses) e retorna o tipo dela, vamos testar.

```javascript
var exemploNumero = 34 // Number integer
var exemploTexto = "Trinta e quatro ☕" // String
var exemploBooleano = true // Boolean

console.log(typeof(exemploNumero)) // "number"
console.log(typeof(exemploTexto)) // "string"
console.log(typeof(exemploBooleano)) // "boolean"
```

## Deixe seu feedback!
Por hoje é isso, espero que tenham entendido e se tiverem qualquer dúvida, sugestão ou correção, fiquem à vontade para deixar nos comentários que eu respondo assim que possível.