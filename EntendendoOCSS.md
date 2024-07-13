## Disclaimer

Nesse artigo vou abordar o CSS com minhas próprias palavras, e tentar explicar para alguém que nunca teve contato com desenvolvimento web, mas quer saber mais sobre, o que é e como ele funciona.

Caso você tenha alguma dúvida ou correção de algum conceito, por favor, não deixe de escrever nos comentários.

Vamos lá...

# O que é CSS

CSS significa _Cascading Style Sheets_ ou _Folhas de estilo em cascata_ em português.
Folhas de estilo porque são os documentos CSS que definem regras de estilo para os documentos HTML.
E em cascata porque os estilos vão sobrepor os outros durante o documento, isso ficará mais claro em breve...

E sim, esse artigo terá exemplos com HTML, então se você ainda não sabe o que é, recomendo ler [esse artigo](https://dev.to/joaopedrov0/entendendo-o-html-2c36) que eu escrevi para explicar, assim como estou fazendo aqui com CSS, o que é o HTML e pra que ele serve.


![Cascata](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/uobsw3i9fy7nklpqho5h.jpg)

No CSS, a sintaxe que usamos é a seguinte:

```
seletor{
    propriedade: valor;
}
```
* O **Seletor** vai identificar quem deve obedecer as regras dentro das chaves.

* A **Propriedade** determina o que será mudado.

* O **Valor** determina como essa propriedade será alterada.

Por exemplo, podemos usar o **seletor** para selecionar uma **tag** `<p>` com um conteúdo dentro, e definir que a **propriedade** "cor do texto" será alterada para o **valor** vermelho.

O código ficaria assim

index.html:
```
<link rel="stylesheet" href="style.css">
<p>Um texto qualquer</p>
```

style.css:
```
p{
    color: red;
}
```
Resultado:
![Resultado do exemplo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qjwi1wcra6mpnio3t9kr.png)

A tag `<link>` serve para conectar o nosso arquivo `style.css` ao arquivo html, para que os estilos sejam aplicados.
E é exatamente sobre isso que eu vou falar agora!

## Formas de aplicar regras de estilo no HTML

### Tag `<link>`
É a mesma forma usada no exemplo.
### Tag `<style>`
Você pode, dentro do HTML mesmo, usar essa tag para escrever estilos CSS sem ter que criar um arquivo `.css`

```
<style>
    p{
        color: red;
    }
</style>
```
### Propriedade `style`
Você pode usar a propriedade `style` do elemento para definir estilos que serão aplicados nele.
> Usar essa forma, aplicará estilo apenas no elemento que você colocar, das outras formas, todos os elementos `<p>` serão afetados.

```
<p style="color: red;">Um texto qualquer</p>
```

Todos funcionam, porém, o mais indicado é o primeiro (criar o arquivo `.css`) por dois motivos.

O método da tag `<style>` é ineficiente pois as vezes você vai precisar separar o seu CSS, para organizar melhor as coisas e que regras são pra quem...

E o método da propriedade é ineficiente pois as regras passadas dentro dele, servirão apenas para aquele elemento, e quando se tem mais elementos você teria que colocar as propriedades um por um.
### Usando a propriedade `style`
![Exemplo inline style](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/64iny2hzazsgwoh3zco5.png)
![Resultado inline style](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rhmttn42h7wsgmf3shjo.png)
### Usando a tag `<style>`
![Exemplo tag style](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hmylc0dfr8h98yxlhinp.png)
![Resultado tag style](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/a9rboqg076sbq28m7kt3.png)

### Usando um arquivo CSS

![Exemplo css externo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/a2noavzo9xv8dhwnll9w.png)
![Resultado css externo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/a9rboqg076sbq28m7kt3.png)


## Por que "cascata"
Observe o código abaixo.
Nesse exemplo, que cor o texto apareceria?
![code cascata](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zescxft6j9sto4dn1fdc.png)
E agora, veja o resultado abaixo
![Result cascata](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/uikgmnszavi0teerqmnz.png)
Talvez você tenha dito que seria o vermelho, pois ele apareceu primeiro... e não, mas porque então?
Vamos retomar algo que eu disse no começo do artigo
> _"E em cascata porque os estilos vão sobrepor os outros durante o documento, isso ficará mais claro em breve..."_

Ou seja, os estilos foram "caindo" em cascata e um sobrepôs o outro, o navegador leu que deveria ser vermelho, e definiu a cor como vermelho, depois leu que deveria ser azul, e definiu como azul... E esse é o resultado final que aparece para nós.

E é isso, espero que tenha ficado claro como ele funciona, mas ainda assim, qualquer dúvida ou sugestão, não deixe de colocar nos comentários.

Obrigado pela atenção e bons estudos!

Créditos de imagem:
Cascata: Imagem de <a href="https://pixabay.com/pt/users/pexels-2286921/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1846424">Pexels</a> por <a href="https://pixabay.com/pt/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1846424">Pixabay</a>
