---
title: Encerrando processos através das portas no Windows
cover-image: windows.jpg
---

Quantas vezes enquanto nós estavámos desenvolvendo algo, veio aquele famoso erro
<!--more--> que a porta já estava sendo 
utilizada e acabavámos ficando horas e horas tentando desvendar esse mistério. Pois então, nessa explicação abaixo eu mostro
à vocês como se livrarem dessa dor de cabeça para sempre! :D

<iframe width="700" height="350" src="https://media.giphy.com/media/Vbu4tonZB1XkiQU1Rj/giphy.gif" frameborder="0" allowfullscreen></iframe>

{% highlight console %}
netstat -ano | findstr :8080
taskkill /PID {número do processo} /F
{% endhighlight %}