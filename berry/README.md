<h1> HTML Templates to VUE3 </h1>

## Templates Free:
<a hidden id="template"></a>
https://html5up.net/
https://freehtml5.co
https://templatemo.com/page/1
https://www.free-css.com/free-css-templates

## Introdução
E ai Dev, espero que esteja bem!

Caso vc não me conheça, eu sou o U3DA e eu tenho o costume de deixar minha vida como DEV cada vez mais facil. E as experiencias q eu vou agregando nos meus desenvolvimentos, eu costumo a melhorar ou ter ideias em cima delas. *Pensar fora da casinha 🪽*

Dessa vez, dps de muitos desenvolvimentos com o VUE, eu comecei a me questionar sobre o quão rápido eu poderia desenvovler por exemplo uma Landing Page.
Nisso eu comecei a bombardear minha cabeça de novas ideas ou organizações que possibilitariam um desenvolivmento mais breve e como eu costumo a usar o Figma pra criar as UI antes de colocar em codigo, eu percebi que essa etapa poderia ser pulada!

*Claro que isso depende primeiramente do que vamos desenvolver e como será conduzido a ideia e validação da pagina com o cliente.*

Lembrando que essa ideia se encaixou perfeitamente para criação de lading pages, mas isso n te impossibilita de **Pensar fora da caixinha**.

### ⭐ Solução ⭐
*- Ok U3DA, chega de enrolação e me mostra essa idéia pra deixar o desenvolvimento mais rapido.*
Calma Cocaino... Antes disso eu queria te relembrar uma parada importante, que no desenvolvimento com o FW(Framework) VUE (e acredito tbm que na maioria dos FW), quando a gente faz a build do projeto final, fica apenas HTML, CSS, e JS.

*Ou seja gordolas, independente do prato de lasanha que tu comeu, no final sempre sai 💩*

Pensando nessa linda analogia, e lembrando dos meus tempos de Word Press, comecei a pesquisar sites que forneciam [Templates](#templates) compilados em apenas HTML, CSS e JS. Com o intuito de poder implementar isso dentro da nossa aplicação em VUE.
Vale lembrar também q por mais q nossos projetos sejam desenvolvidos por padrão com Html, Scss e Ts, a gente ainda consegue reaproveitar tudo do template escolhido.

### Partes do desenvolvimento importantes

#### Vite Init
Como existem alguns tipo desenvolvimento front, vamos focar no SPA pra esse caso.
E pra 2024 vamos usar o vite feshow 🤘🏽
[Doc do Vite](https://vitejs.dev/guide/)

`npm create vite@latest my-vue-app -- --template vue`

Dai a partir daqui tu começa a organizar seu projeto.
Lembre-se de entender como ta o projeto do template pois vc precisara declarar algumas coisas dentro do novo projeto.

#### index.html (./index.html)
Na raiz de todo projeto VUE, a gente sempre vai encontrar esse [index](./index.html), pois ele é a nossa porta de entrada para a nossa pagina.
Sabendo disso a gente declara todos os imports sendo eles CSS e JS, no proprio Index. Aqui da pra perceber tbm, as bibliotecas que ele vai utilizar, como por exemplo o BootStrap.
**Pelo amor de deus, salva s arquivos numa pasta dentro do projeto, no nosso caso eu decidi padronizar a `./src/assets` e separei pelos tipos/extensões dos arquivos(css, js, fonts). E para as bibliotecas externas, salvei em `./src/vendor`.**

##### HINTs
Descobri um macete pra importar alguns arquivos que tem o JS mais Complexo e dependem de a pagina estar totalmente renderizada.
`O uso de defer garante que o script seja baixado durante o carregamento da página, mas seja executado apenas após o HTML ter sido totalmente analisado.`

E ai tu importa no próprio index.html desse jeito assim: `<script src="src/assets/js/jquery.min.js" defer></script>`

#### App.vue (./src/App.vue)
No componente padrão do VUE, aquele primeiro de todos, eu resolvi usar ele como se fosse a pagina principal do template, ou seja aquele HTML gigante que encontra dentro da pagina do template, vem aqui, dentro da tag `<template>`.
Aproveitando o App.vue, aqui tambe'm podemos falar da **Estilização personalizada** da pagina.
Como a gente já importa os arquivos de estilizaçao padrão do template, por necessidade eu descobrir uma outra forma de aplicar estilizações customizadas para a pagina, sem a necessidade de mexer nos arquivos do template. No caso é sempre bom mapear as tags q pretendemos alterar, no caso do Google Chrome eu costumo a utilizar o `Ctrl + Shift + C` pra inspecionar os elementos que eu quero alterar.
E por padrão das paginas feitas em VUE, haverá o **id = app** no index.html citado acima.
Com isso é importante sempre declarar todas as modificações de estilo dentro do id *#app*.

Exemplo:

*App.vue (./src/App.vue)*
```
    <style lang="scss">
        #app{
            .icon{
                background-color: aqua;
            }
        }
    </style>
```# berry
