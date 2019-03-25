---
title: Acer Cloudbook 11
author: Emanuel Diego S Penha
date: '2016-02-03'
slug: acer-cloudbook-11
categories:
  - gear
tags: []
header:
  caption: ''
  image: ''
---

Pensando na minha volta ao Brasil, comecei a procurar um substituto para o 
macbook air com o qual trabalho.
Não tenho o que reclamar do case em alumínio, do teclado, do tempo de bateria. 
Enfim, o mac que uso é melhor do que tudo o que eu já usei a nível de notebooks.

Mas várias pequenas coisas me aborrecem aqui e acolá. Os updates nem sempre saem 
como esperado. Sempre tem algo que acaba deixando de funcionar. O último 
problema que tive foi com o homebrew. A minha instalação deixou de funcionar com
o El Capitan. Depois de quebrar muito a cabeça com o novo modo de segurança 
noroot da apple, acabei desistindo e voltando para o macports.

Então estava pensando em comprar um chromebook, uma vez que eu poderia instalar 
uma distro e ter uma máquina leve, com alto tempo de bateria e principalmente 
barata. Até que me deparo com uma promoção do Acer Cloud Book.

Tive alguma dor de cabeça para instalar outras distros, mas o xubuntu rodou sem 
maiores problemas.

A única coisa que tive que fazer a mais foi seguir os passos para instalar o 
archlinux que achei nessa [página](https://wiki.archlinux.org/index.php/Acer_Cloudbook).

Primeiro tive que adicionar `edd=off noapic modprobe.blacklist=pinctrl_cherryview` 
durante o boot da imagem de instalação. Depois, mudar a linha que define essas
mesmas opções no arquivo `/etc/default/grub`. É só procurar a linha que começa 
com `GRUB_CMDLINE_LINUX` e editá-la para que fique como a linha abaixo.

`GRUB_CMDLINE_LINUX="quiet edd=off noapic modprobe.blacklist=pinctrl_cherryview` 

O desempenho é bom, considerando o preço. Não consigo abrir mais do que 4 ou 5
páginas no google chrome de maneira confortável. Tentei firefox e Ópera, mas 
ambos se mostraram muito mais lentos. Fora isso, não tenho do que
reclamar do meu pequeno notebook.
