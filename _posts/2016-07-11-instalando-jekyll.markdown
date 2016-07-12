---
title: Instalando o Jekyll na sua máquina
cover-image: easy.jpg
---

E aí pessoal, vim aqui como prometido há alguns posts atrás como fazer a configuração do Jekyll

<!--more-->

Antes de começarmos, vou explicar o que é exatamente o Jekyll. 

Jekyll é um gerador de conteúdo estático, muito indicado para sites e blogs (como foi o meu caso). A formatação de textos e posts é baseado no [Markdown](https://daringfireball.net/projects/markdown/) e um padrão de template chamado [Liquid](https://shopify.github.io/liquid/). 

Vamos lá para a instalação:

* O sistema operacional onde vai ser feito a configuração será no Windows, não cheguei a fazer em outros sistemas operacionais mas é possível ser a mesma coisa.

1 - Instalando o Ruby e o Ruby DevKit

Jekyll foi desenvolvido em Ruby mas você não precisa saber essa linguagem quando for produzir seu conteúdo desejado. Já o DevKit é necessário pois algumas depedências do Jekyll são acessadas por lá.

- Acesse esse [link](http://rubyinstaller.org/downloads/) para baixar o Ruby. Baixe a versão x86 ou x64 de acordo com o seu sistema operacional. Instale a última versão, que atualmente é 2.3.0

Depois de baixá-lo, preste atenção durante a etapa de instalação e marque a opção "Add Ruby executables to your PATH" como é mostrado na imagem abaixo

![ruby-path](http://i.imgur.com/mPALavC.png?1) <small>Source: [imgur.com](http://i.imgur.com/mPALavC.png?1)</small>

Agora já podemos instalar o DevKit, através deste [link](http://rubyinstaller.org/downloads/). O arquivo começa com DevKit-mingw64, só diferenciando a arquitetura de 32 ou 64 bits. Agora que já baixamos, ele pedirá em qual local ele deve ser extraído. Eu prefiro colocar diretamenta na raíz para não ter problemas.	

![devkit](http://image.prntscr.com/image/76d4347ea40448cca871755567678387.png)
<small>Source: [prnt.sc](http://image.prntscr.com/image/76d4347ea40448cca871755567678387.png)</small>  

Muito bem, após isso vamos para o prompt configurar mais algumas opções:

![config1](http://image.prntscr.com/image/b421f6671cb2413f83ddb550264d5d95.png)
<small>Source: [prnt.sc](http://image.prntscr.com/image/b421f6671cb2413f83ddb550264d5d95.png)</small> 

Depois disso, você precisa associar o DevKit com o Ruby. Então vá para a pasta do DevKit e edite o config.yml, acrescentando essa linha como na imagem abaixo:

![config2](http://image.prntscr.com/image/f86446d70f224bcd9e7b2ccd494e1f7a.png)
 <small>Source: [prnt.sc](http://image.prntscr.com/image/f86446d70f224bcd9e7b2ccd494e1f7a.png)</small> 
 
Volte para o prompt de comando e execute isso:

![config3](http://image.prntscr.com/image/20db26b2f6574f55b8db0b128752cdb9.png)
 <small>Source: [prnt.sc](http://image.prntscr.com/image/20db26b2f6574f55b8db0b128752cdb9.png)</small> 

Depois disso só digitarmos dessa forma no prompt:

{% highlight bash %}
gem install jekyll
jekyll new meublog
cd meublog
jekyll s
# => Navegue através do endereço http://localhost:4000
{% endhighlight %}

Quem quiser dar uma olhada mais a fundo, pode acessar o site do [Jekyll](https://jekyllrb.com/) para tirar suas dúvidas.

E pronto, o Jekyll já está funcionando e o projeto já está localmente no ar :)