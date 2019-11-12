---
title: Configurando Eslint + Prettier no seu VS Code
cover-image: camping.png
---

Sempre quando eu programo, imagino como o código deve ser legível para outra pessoa
tentar entender o que está acontecendo. E cá entre nós, é horrível quando lemos um
código de uma outra pessoa sem nenhum tipo de padronização.
{: style="text-align: justify"}
<!--more-->

Agora imagine quando estamos trabalhando com o um time e cada pessoa a sua própria 
maneira de programar, cada um com seu ambiente diferente. Por causa desse motivo, 
surgiram os **styles guides** para melhorar tanto a formatação, entendimento, 
consistência e principalmente manutenção de qualquer projeto.
{: style="text-align: justify"}

## [Eslint](https://eslint.org/)
É uma ferramenta de análise de código estática para identificar padrões 
problemáticos encontrados no código JavaScript.
{: style="text-align: justify"}

## [Prettier](https://prettier.io/)
É um formatador de código opinativo que suporta muitas linguagens que remove todo
o estilo original e garante que todo o código emitido esteja em conformidade com
um estilo consistente.
{: style="text-align: justify"}

Então vou mostrar à você toda a configuração necessária para utilizar o Eslint
juntamente com o Prettier.
{: style="text-align: justify"}

Eu deixei um projeto pronto no meu [Github](https://github.com/raphabarreto/eslint-prettier)
caso você se perca ou estiver com alguma dúvida ou problema.
{: style="text-align: justify"}

Vamos criar um novo projeto. Crie uma nova pasta e coloque o nome que achar melhor,
no meu caso coloquei eslint-prettier e abra essa pasta no seu VS Code.
{: style="text-align: justify"}

![](https://i.imgur.com/OkdjdLt.png)

Clique no botão "Install" o [Eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
e também o [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode),
assim um alerta aparecerá para abrir através do VS Code ou se preferir, pesquise
através das extensões no próprio VS Code.
{: style="text-align: justify"}

Agora vamos criar uma pasta no diretório raiz chamada src e dentro dela, um arquivo
chamado index.js.
{: style="text-align: justify"}

<img src="https://i.imgur.com/Q5fpfdo.png" alt="printing" >

No index.js, vamos digitar esse trecho só para exemplo de formatação

{% highlight javascript %}
function digaOla(nome )  {
  return `Olá, ${nome }`
}

console.log(digaOla('Raphael'))
{% endhighlight %}

Podemos perceber que está faltando ; e existem alguns espaços a mais de propósito
para vermos como as essas 2 ferramentas vão trabalhar em cima disso.
{: style="text-align: justify"}

Agora no seu terminal, instale via [Yarn](https://yarnpkg.com/pt-BR/) o Eslint
{% highlight console %}
yarn add eslint -D
{% endhighlight %}

**Não se esqueça de colocar -D no final para instalarmos no modo desenvolvimento.**
{: style="text-align: justify"}

Depois, basta rodar esse comando abaixo e série de opções vão ser mostradas.
{: style="text-align: justify"}
{% highlight console %}
yarn run eslint --init
{% endhighlight %}

Escolha as opções como na imagem a seguir
![](https://i.imgur.com/9COFPsd.png)

E por fim, este último comando, pois não vamos instalar o AirBnB Guide através do
npm como foi perguntado acima, e sim atráves do Yarn.
{: style="text-align: justify"}

{% highlight console %}
yarn add eslint-config-airbnb-base eslint-plugin-import eslint -D
{% endhighlight %}

Depois de tudo instalado, 3 novos arquivos irão aparecer na pasta raiz do projeto.
{: style="text-align: justify"}
<img src="https://i.imgur.com/5MRrYlY.png" alt="printing" >

O arquivo .eslintrc.json contém todas as regras de validação que você queira
para o seu código, por enquanto não vamos alterar nada.
{: style="text-align: justify"}

Agora basta digitarmos esse código no terminal e o Eslint realizará toda a correção
automaticamente e o arquivo ficará com a formatação correta. Após o --fix, colocamos
o caminho que queremos e --ext as extensões dos arquivos que queremos a formatação.
{: style="text-align: justify"}

{% highlight console %}
yarn eslint --fix src --ext .js
{% endhighlight %}

E esse será o resultado final:
{: style="text-align: justify"}

![](https://i.imgur.com/qpebTKr.png)

Provavelmente no termina, pode dar esse seguinte aviso:

{% highlight console %}
5:1  warning  Unexpected console statement  no-console

✖ 1 problem (0 errors, 1 warning)

Done in 1.04s.
{% endhighlight %}

Para desabilitar esse erro, basta colocar essa opção lá naquele arquivo .eslintrc.json
e rodar o comando novamente e assim não aparecerá mais.
{: style="text-align: justify"}

![](https://i.imgur.com/IVxxNi4.png)

Caso queira ver mais regras, bastar acessar a [documentação do Eslint](https://eslint.org/docs/rules/).

Ufa né? Mas e o Prettier, pra que vou utizá-lo? O Prettier atua enquanto estamos
programando. Como foi explicado acima, é uma ferramenta opinativa e logo quando
você sempre salva o arquivo que está editando, já acontece toda a formatação
automaticamente. Enquanto que no Eslint, existe todo o processo de "escanear" o
caminho, verificação de erros de sintaxe e uso do style guide que você pré definiu.
{: style="text-align: justify"}

Para a sua instalação, bastar rodar isso abaixo no seu terminal

{% highlight console %}
yarn add prettier eslint-config-prettier eslint-plugin-prettier -D
{% endhighlight %}

Após a instalação completa das dependências, crie um arquivo na raiz do projeto
chamado .prettierrc e dentro dele, coloque essas configurações:
{: style="text-align: justify"}

{% highlight json %}
{
  "singleQuote": true,
  "trailingComma": "es5"
}
{% endhighlight %}

Agora volte naquele arquivo .eslintrc.json e acrescente as informações a seguir:
{: style="text-align: justify"}

{% highlight json %}
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es6": true
    },
    "extends": [
        "airbnb-base",
        "prettier"
    ],
    "plugins": [
        "prettier"
    ],
    "globals": {
        "use": "readonly",
        "Atomics": "readonly",
        "SharedArrayBuffer": "readonly"
    },
    "parserOptions": {
        "ecmaVersion": 2018
    },
    "rules": {
        "prettier/prettier": "error",
        "no-console": "off"
    }
}
{% endhighlight %}

Veja que acrescentamos 3 opções em relação ao original.
* "extends" -> "prettier"
* "plugins" -> "prettier"
* "rules" -> "prettier/prettier": "error"

Podemos voltar para o index.js e ao apagarmos as ; ou colocarmos algum espaço a 
mais já é sinalizado o erro e quando salvamos o arquivo, todos os erros são
corrigidos automaticamente.
{: style="text-align: justify"}

Quem quiser saber mais, bastar entrar na [documentação do Prettier](https://prettier.io/docs/en/).

É uma configuração extensa, eu sei. Mas vale a pena pois vai te poupar de muitas
frustrações que irá passar.
{: style="text-align: justify"}

Espero que isso seja de grande ajuda e por favor, comente se o post ficou claro
ou se teve alguma parte que ficou confusa. 
{: style="text-align: justify"}

Eu só melhoro e subo mais um degrau, graças a sua opinião. Muito obrigado! ❤️
{: style="text-align: justify"}
