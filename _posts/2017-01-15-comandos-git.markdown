---
title: Comandos úteis no git
cover-image: git.png
---

Olá pessoal, estou aqui para trazer uma lista de comandos a medida que está trabalhando com git.
Mas antes de tudo, vamos com uma breve introdução do que é o Git.

<!--more-->

## História

Git é um sistema de controle de versão. Quem o criou foi nada mais e nada menos que Linus Torvalds,
criador do Linux. Mas qual foi a motivo dela ter aparecido? Existia uma empresa chamada BitKeeper
que versionava todo o código do Linux. Mas aconteceu algumas alterações e o Linux deixaria de ser isento 
para continuar mantendo o seu código lá dentro. Torvalds foi contra tudo isso e acabou criando o git,
com várias melhorias comparadas ao seu antecessor.

Vamos lá:

| Comando  | Função  | Exemplo |
------------ | ------------- | --------------- 
| git config    | Configura valores para serem usados como usuário, email e etc | git config --global user.name "Meu nome" 
| git add | Adiciona os arquivos no seu diretório de trabalho para a index      |    git add . |
| git rm  | Remove os arquivos de sua index e seu diretório de trabalho	e eles não estarão no "tracked" | git rm arquivo
| git commit | Analisa todas as novas alterações e salva em um novo objeto para ser realizado a atualização | git commit -am "Novo commit" |
| git status | Mostra o status dos arquivos na sua index em relação ao diretório de trabalho | git status |
| git branch | Lista todos os seus branches disponíveis, inclusive os remotos | git branch |
| git checkout | Troca para o branch que deseja trabalhar | git checkout branch |
| git tag | Cria uma tag para um commit específico | git tag -a 1.0.0 -m 'Versão 1.0.0' |

### Links importantes

* [Git - guia prático](http://rogerdudler.github.io/git-guide/index.pt_BR.html)
* [Curso de Git e Github para Iniciantes](Githttp://willianjusten.teachable.com/courses/enrolled/git-e-github-para-iniciantes)
* [Mais comandos](https://www.siteground.com/tutorials/git/commands.htm)

Recomendo fortemente vocês darem uma olhada pois são complementos que irão clarear ainda mais as dúvidas. Git é uma ferramenta muito importante no mercado, e é praticamente obrigatória para qualquer profissional nessa área. Espero que tenham gostado e se tiverem alguma dúvida e sugestões, podem comentar aqui embaixo. Até a próxima ;)