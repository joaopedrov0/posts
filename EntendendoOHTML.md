## Antes de começar, um disclaimer
Nesse artigo vou abordar o HTML com minhas palavras, e tentar explicar para alguém que nunca teve contato, mas quer saber mais sobre, o que é e como ele funciona.

Caso você tenha alguma dúvida ou correção de algum conceito, por favor, não deixe de escrever nos comentários.

Vamos lá...

## O que é?

HTML é, na verdade, uma abreviação para _HyperText Markup Language_, ou em português, _linguagem de marcação de hipertexto_. Usando a estrutura HTML você pode construir páginas web.

### E qual é essa estrutura?

Simples, ela é definida por tags, que por sua vez tem o **nome do elemento**, seus **atributos**, e seus "filhos" ou **children**.

`<elemento atributo="valor">...</elemento>`

Nesse caso, a tag pode ter **childrens** associados a ela, mas algumas vezes, nós não precisamos desses childrens, e se esse for o caso, usamos o auto-fechamento de tags

`<elemento atributo="valor" />`

### Exemplos com tags

Para demonstrar, vou te mostrar duas tags que abrem e fecham (E podem ter childrens), e duas com auto-fechamento.


#### Que "Abrem e fecham"

```
<p>Hello World!</p>
```
A tag `<p>` serve para demarcar parágrafos, dentro dela você pode escrever o conteúdo que quer exibir.

```
<a href="https://github.com/joaopedrov0">GitHub</a>
```
A tag `<a>` é usada quando queremos criar um link. Nesse caso temos o **nome do elemento** `a`, um **atributo** `href` (_HyperText Reference_), e o **valor** do atributo é o link para o meu GitHub.


E ainda no exemplo da tag `<a>`, a palavra `GitHub` é o **children**, nesse caso foi um texto, mas childrens podem ser outras tags também.



#### Com auto-fechamento (_self closing tags_)
```
<img src="patinho.png" />
```
A tag `img` serve para inserir uma imagem.
Nesse exemplo, `img` é o **nome do elemento**, `src`(source) é um **atributo** e o **valor** desse atributo é o nome do arquivo da imagem que eu quero exibir.

## E esse é o conceito de tags!

Com esse conceito, agora basta entender individualmente algumas tags, e usar isso para estruturar os documentos HTML.
...
Com os conceitos que eu acabei de apresentar, eu construí um exemplo final:
```
<h1>Hello World</h1>
<h2>Um parágrafo aleatório:</h2>
<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
<a href="https://github.com/joaopedrov0">E um link</a>
```
Eu salvei esse código em um arquivo `.html` e abri ele no navegador... E o resultado é esse!

![Exemplo final](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zsrijof7b4b8fwvtsn10.png)
E nesse momento, pode ser que você esteja com duas perguntas...

> O que era aquela tag "h1" e "h2" no seu exemplo?

Bem, essas são tags de título, tanto a h1 quanto a h2.
O número que vem depois da letra "h", é pra definir a **importância daquele conteúdo na sua página**, quanto **maior** o número, **menor** a importância e vice-versa! Sendo o h1 o mais importante, geralmente o título principal da sua página, ou em alguns casos o seu logo, e o h6 o título com menor relevância.

> E que troço horroroso é esse resultado?! Você não disse que isso é usado para construir páginas web? Eu nunca vi uma página assim!

Bem observado, realmente a aparência não ficou das melhores, mas é pra isso que serve uma outra linguagem, o **CSS** (_Cascading Style Sheets_), que é usado para definir cores, posições, tamanhos, fontes, etc. Depois de ler esse artigo, não deixe de ler [esse outro](https://dev.to/joaopedrov0/entendendo-o-css-47in) que eu escrevi sobre CSS.

E é isso! Espero que tenha entendido, qualquer dúvida, não deixe de colocar nos comentários.

Bons estudos, e até mais!



Créditos da imagem de cover
Imagem de <a href="https://pixabay.com/pt/users/jamesmarkosborne-1640589/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1076536">James Osborne</a> por <a href="https://pixabay.com/pt/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1076536">Pixabay</a>
