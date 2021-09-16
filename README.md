# ExampleBot

Esse bot retwita o ultimo tweet usando a hashtag  ["`#mediaarts`"][twitter-mediaarts] e tenta retwitar uma vez por hora.


_Nota:Voce tem que estar preparado para usar a interface de linha de comando do seu computador para usar esse bot. Se voce nunca utilizou ela,tem alguns tutoriaiis para [macOS]
(http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) e [Windows](http://www.bleepingcomputer.com/tutorials/windows-command-prompt-introduction/)._

## Instalação
Instale o [Node.js](http://nodejs.org/). 

Crie um diretorio de projeto vazio conveniente para voce e [baixe o arquivo compactado em zip](https://github.com/masuta16/examplebot/archive/master.zip), 
depois descompacteos conteudos para o diretorio do seu projeto. Vá para o diretorio do seu projeto na linha d ecomando devem haver 4 arquivos lá:  `.gitignore`, `README.md`, `bot.js` and `config.js`. 
Então digite nesse diretorio:

`npm install twit`

Ele instala codigos para o subdiretorio `npm_modules`, entre elas o Twit que é a biblioteca que fala com o Twitter.


## Conectando ao Twitter


Nesse ponto voce precisa registrar uma conta no Twitter e tambem pegar a "app info".

Então crie uma conta no Twitter para qualquer conta que voce quer twitar suas coisas. O  Twitter não permite que voce registre multiplas contas de twitter no mesmo endereço de email. Então eu te recomendo a criar um novo endereço de email para a conta do Twitter. Quando voce refistrar a conta para esse endereço de email, aguarde pelo email de confirmação. Então loge na sua conta do twitter para seu bot nesse link:

https://apps.twitter.com/app/new

Uma vez nesse  site, complete nos campos requeridos com: name, description,website. Nada disso realmente importa no seu atual aplicativo é só para a informação no Twitter. Preencha o captcha e faça a submissão. 
Depois voce vai ver uma tela com uma aba chamada "Details". Clique na opção "Settings" e sobre "Application Type" escolha "Read and Write" então clique no botão de atualizar no topo.
Vá para a aba de Tokens e acesso e no botão clique em "create my acess token". Nada vai acontecer de imediato. Então aguarde um minuto e recarregue a pagina. Deve aparecer o "acess token" e "acces toke secret" que são textos com letras e numeros.

Use um editor de texto para abrir o arquivo "config.js". Ele deve ter uma aparência como essa:

```javascript
module.exports = {
  consumer_key:         'blah',
  consumer_secret:      'blah',
  access_token:         'blah',
  access_token_secret:  'blah'
}
```
Ao inves de `'blah'` coloe as informações apropriadas da pagina "Details". Essa é a informação de login essencial para o seu app.
Digite o seguinte comando na sua linha de comand dentro do diretorio do  seu projeto:

`node bot.js`

Felizmente nesse ponto voce verá uma mensagem como "Sucess! Check your bot, it should have retweeted something." Verifique a conta do Twiter para seu bot, e ele deve ter retwitado um tweet com a hashtag #mediaarts.

[twitter-mediaarts]:https://twitter.com/hashtag/mediaarts
