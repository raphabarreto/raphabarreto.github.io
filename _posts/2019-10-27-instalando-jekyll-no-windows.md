---
title: Instalando Jekyll no Windows
cover-image: autumn.png
---


Eu já tinha feito um post de como fazer essa instalação mas já estava beeeem desatualizada. Então
estava na hora de refazer tudo e hoje em dia é bem mais descomplicado do que antigamente. Bom, vamos
lá para o passo a passo:
{: style="text-align: justify"}

<!--more-->

Entre no site do [Ruby](https://rubyinstaller.org/downloads/) e baixe a última versão na categoria **WITHOUT DEVKIT**.


<img src="https://i.imgur.com/gSJFFUy.png" alt="printing">

**Observação -> Atualmente o [Jekyll](https://github.com/jekyll/jekyll/releases/tag/v4.0.0) está na versão 4.0, então não suporta versão anteriores do Ruby 2.4.**

Após ter baixado, comece a instalação e lembre-se de marcar estas opções:

<img src="https://i.imgur.com/SRxBAIM.png" alt="printing" >

E logo no final da instalação, marcar essa opção também:

<img src="https://i.imgur.com/1sMgFii.png" alt="printing" >

Após isso, uma nova janela irá abrir para a instalação do MSYS2:

<img src="https://i.imgur.com/2A8xnDY.png" alt="printing" >

O [MSYS2](https://www.msys2.org/) é uma plataforma desenvolvida para o Windows que atualmente substitui o antigo DevKit que foi construído em cima do MSYS1 que hoje em dia não está sendo mais mantido.
{: style="text-align: justify"}

Instale as 3 opções, uma a uma de cada vez.

Logo na opção 1º, siga o famoso clássico next, next, next:


<img src="https://www.msys2.org/1_msys32-start.png" alt="printing" >

<img src="https://www.msys2.org/2_msys32-install_path.png" alt="printing" >

<img src="https://www.msys2.org/5_msys2-finish_install.png" alt="printing" >

Não esqueça de desmarcar "Run MSYS2 now"

E assim vamos para a segunda e terceira instalação, tudo sendo feito através do prompt.

Agora bastar rodar esse comando para fazer a instalação do Jekyll:

{% highlight console %}
gem install jekyll bundler
{% endhighlight %}

Verifique se está tudo em ordem instalado, como abaixo:

<img src="https://i.imgur.com/9P9aUdL.png" alt="printing" >

E é isso, é um tutorial extenso que deve ser seguido com calma. Qualquer dúvida, deixa aqui embaixo nos comentários que eu vou te ajudar com todo prazer! ;)
{: style="text-align: justify"}