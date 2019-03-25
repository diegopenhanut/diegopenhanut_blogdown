---
title: Migrando para Hugo
author: Emanuel Diego S Penha
date: '2018-08-07'
slug: migrando-para-Hugo
categories:
  - programação
tags: []
header:
  caption: ''
  image: ''
---

Resolvi mudar o modo com o qual escrevo (pouco, devo admitir) o blog. Antes estava
usando [Jekyll](https://jekyllrb.com/). Embora ache que ele cobre minhas necessidades, toda vez que tinha que 
instalar/configurar o [Ruby](https://www.ruby-lang.org/pt/), acabava investindo tempo demais. A experiência como um todo
não era satisfatória.

Então experimentei o [blogdown](https://bookdown.org/yihui/blogdown/), pacote para R do [Yihui Xie](https://yihui.name/en/). O pacote é um wrapper
para Hugo e facilita bastante sua configuração, criação de posts, inserção de 
figuras. Conversa muito bem com o Rstudio mesmo que o uso dessa IDE não seja obrigatório.

A ideia desse post é documentar como foi essa transição.

# Tema e idioma

O tema que estou usando é o [Academic](https://themes.gohugo.io/academic/). 

Para mudar para português, edite `config.toml` e adicione:

`defaultContentLanguage = "pt"`

`languageCode = "pt"`

Mas isso não muda o idioma da `menu bar` 

Então voltamos para a edição `config.toml`. Mudei `publications` `publications_selected` para publications por que não tenho uma grande quantidade de artigos, então removi essa parte.

```
[[menu.main]]
  name = "Home"
  url = "#about"
  weight = 1

[[menu.main]]
  name = "Publicações"
  url = "#publications"
  weight = 2

[[menu.main]]
  name = "Posts"
  url = "#posts"
  weight = 3

[[menu.main]]
  name = "Projetos"
  url = "#projects"
  weight = 4

[[menu.main]]
  name = "Ensino"
  url = "#teaching"
  weight = 5

[[menu.main]]
  name = "Contato"
  url = "#contact"
  weight = 6
```

# Deploying

A primeira coisa que fiz foi `git clone` minha página antiga. Daí, adicionar o caminho da página pessoal como diretório de publicação. No meu caso, foi colocar 
`publishDir= "../diegopenhanut.github.io"` no `config.toml`. Quando o 
site for construído/atualizado, o html será depositado no diretório. 
Depois disso é `git push origin master`

# Mensagens de erro

Uma última observação é que as mensagens de erro no Rstudio nem sempre aparecem. Em uma vez específica, tive que usar o terminal, digitando o comando `hugo -v` para ver o que havia acontecido e daí, com a mensagem de erro, concertá-lo.