# glio.js
Detecte se o mouse do usuário for para as bordas do viewport/documento de seu site ou sair dele, e quando isso acontecer, dispare um callback.

####  Como Funciona: <a href="http://luisvinicius167.github.io/gliojs/"> Demo </a>

### Razões para uso:
* Aumentar suas taxas de conversão!
* Dar aos visitantes razões para ficar!
* Atrair a atenção de seus usuários!


## Como instalar:
#### Manual:
* Importe a biblioteca glio.min.js que está na pasta 'dist' dentro do seu site ```<script src='glio.min.js'></script>``` 

#### Instale usando o Bower:
* ``` bower install glio.js ```

## Uso:
Os argumentos são passados como um Array, onde o primeiro argumento dentro do array é a direção e o segundo é o callback. Você pode colocar até 5 arrays com cada posição dentro do método init. <br>
```glio( [ direction, callback ] )```.

## Direções:
* top
* top-left
* top-right
* bottom-left
* bottom-right

## Exemplos:
* Direção top-left e top-right
```
    glio.init(
      [ 'top-left', function () {
          alert('this is top-left');
        }
      ],
      [ 'top-right', function () {
          alert('this is top-right');
        }
      ]
    );
```

* Todas as direções
```
  glio.init(
    [ 'top', function () {
        alert('this is top.');
      }
    ],
    [ 'top-left', function () {
        alert('this is top-left');
      }
    ],
    [ 'top-right', function () {
        alert('this is top-right');
      }
    ],
    [ 'bottom-left', function () {
        alert('this is bottom-left');
      }
    ],
    [ 'bottom-right', function () {
        alert('this is bottom-right'); 
      }
    ] 
  );
```

## Configurações:
  ```glio.config.key = value;``` Registre as configurações antes do método <i>init</i>. 
 * screenWidthFragment: a quantidade de partes que a largura da tela será dividida. <i>Valor padrão: 12.</i>
 * centerTopHeight: altura da direção 'top'. Quando o mouse do usuário tiver a altura menor ou igual a esse valor, o callback será disparado. <i>Padrão: 10.</i>
 * heightTopLeft: altura da direção 'top-left'. Quando o mouse do usuário tiver a altura menor ou igual a esse valor, o callback será disparado. <i>Padrão: 30.</i>
 * heightTopRight: altura da direção 'top-right'. Quando o mouse do usuário tiver a altura menor ou igual a esse valor, o callback será disparado. <i>Padrão: 30.</i>

### Veja a demonstração <a href="http://luisvinicius167.github.io/gliojs/"> aqui</a>.

MIT license.
