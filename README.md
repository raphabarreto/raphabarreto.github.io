# Holo Alfa Jekyll template #

![Screenshot](http://image.prntscr.com/image/99f24910b9534029afe509f283f07936.png)

Holo Alfa é um template minimalista e responsivo feito em Jekyll com foco na legibilidade do conteúdo. Lembrando que este template foi feito pelo Stijn, eu somente fiz algumas alterações.

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

If you're new to Jekyll, check out http://jekyllrb.com/ and read up on Jekyll. It's worth it.

* [Another great resource to learn about Jekyll](http://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
* [Github's guide to using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/)

If you run one of the latest versions of Jekyll, this theme will work with no* problems.

### Installing ##

As simple as forking the repository, and then clone it so you can edit the files locally.

### Configuration ###

Edit `_config.yml`!

You can find `_config.yml` in your site's root directory. This configuration file contains some necessary settings and some optional customization settings. **All settings are explained in `_config.yml` itself.**

There are some customizations that can't be done in `_config.yml`. These include:

* Editing the About, Contact and Archive page.
* Adding or removing pages from the navigation. This can be done in `\_includes\navigation.html`.
* The "thanks" page after a message has been send through the contact page: `thanks.md`
* The gradient on cover images: `\_includes\gradient.css` (this is explained in `_config.yml`).

Also make sure to replace the placeholder favicons and the `\img\og-image.jpg` with your own.

### Start the Jekyll server ###

Run this command at the root of your site:

```
$ jekyll serve
```

> To run Jekyll in a way that matches the GitHub Pages build server, run Jekyll with Bundler. Use the command `bundle exec jekyll serve`.

When everything is OK, your site should now be available at `http://localhost:4000`.

That's it.

---

[MIT license](http://opensource.org/licenses/MIT)
