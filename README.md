# Holo Alfa Jekyll template #

![Screenshot](https://i.snag.gy/v5Gelw.jpg)

Holo Alfa é um template minimalista e responsivo feito em Jekyll com foco na legibilidade do conteúdo. Lembrando que este template foi feito pelo [Stijn](https://github.com/steinvc), eu somente fiz algumas alterações.

Você pode vê-lo em ação: https://raphabarreto.com.br/

## Principais características ##

* Responsivo em qualquer aparelho
* Conteúdo CSS bastante extenso
* Videos responsivos (utilizando [FitVids.JS](http://fitvidsjs.com/))
* Suporte para autores e convidados
* Tempo de leitura dos posts
* Comentários através do Disqus
* Automático [og metadata](http://ogp.me/)
* Arquivamento de páginas automático (sem o auxílio de plugins)
* Automatic sitemap en RSS feed
* Página de contato (com envio de e-mail funcionando perfeitamente)
* Muitas opções de customização (todas encontradas no arquivo `_config.yml`)

E muito mais.

## Primeiros passos ##

Se você é novo utilizando o Jekyll, veja mais informações através http://jekyllrb.com/ e aprenda mais. Vale muito a pena. Recomendo também http://jekyll-windows.juthilo.com/ para aqueles que procuram um passo a passo mais simples. 

* [Outro grande recurso para ser aprendido](http://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
* [Guia do Github mostrando como utilizar Jekyll com Github Pages](https://help.github.com/articles/using-jekyll-with-pages/)

Se você está rodando nas últimas versões do Jekyll, este template irá funcionar sem problemas.

### Instalando ##

Basta dar um fork no repositório, e depois cloná-lo para você poder editar os arquivos localmente da forma que preferir.

### Configuração ###

Edite o arquivo `_config.yml`!

Você pode achar o arquivo `_config.yml` no diretório raiz do projeto. Este arquivo de configuração contém algumas configurações necessárias e algumas configurações de personalização opcionais. **Todas as configurações são expicadas no próprio arquivo `_config.yml` .**

Entretanto, há algumas customizações que não podem ser alteradas no `_config.yml`, que são:


* Edição das páginas About, Contact e Archive.
* Adicionar ou remover páginas de navegação. Isto pode ser feito em `\_includes\navigation.html`.
* A página "obrigado" depois da mensagem que é enviada através da página de contato é localizada no arquivo: `thanks.md`
* O efeito gradiente nas imagens de capa para os posts: `\_includes\gradient.css` (isto é explicado no `_config.yml`).

Se quiser, você pode substituir os favicons e `\img\og-image.jpg` pelo os da sua preferência

### Subindo o seu projeto ###

Execute este comando na raíz do seu projeto:

```
$ jekyll s
```

Quando tudo estiver OK, seu projeto vai estar disponível em `http://localhost:4000` ou em `http://127.0.0.1:4000/`.

Agradecimentos ao criador deste template [Steinvc](https://github.com/steinvc). 

Este é o [repositório](https://github.com/steinvc/holo-alfa) do projeto original e você pode também pode visitar [este outro repositório](https://github.com/steinvc/jekyllthemes) também feito por ele para dar uma conferida em outros templates por curiosidade.

É isso.

---

[MIT license](http://opensource.org/licenses/MIT)
