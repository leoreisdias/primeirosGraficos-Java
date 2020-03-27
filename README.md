# Beginning some Java Graphics concepts for the area of Game Development 
(Começando com alguns conceitos gráficos em Java para Desenvolvimento de Jogos)

## Utilizando de Canvas e JFrames.

Com Canvas defini-se propriedades para a janela do jogo, tal como largura e altura, e para melhor controle uma variavel SCALE auxiliará na manipulação das dimensões.

JFrame trabalha com essas propriedades e pode gerenciar funcionalidades básicas da janela como posição, comportamento ao fechar e abrir, entre outros.


## Contagem de FPS

* A contagem de FPS para melhor precisão é feita simulando nano segundos.
* A cada "NS" segundos será contado um Frame
* Delta armazena o tempo em nano segundos decorrido até alcançar o NS
* Delta vale 1 ao alcançar o tempo de contage e o frame incrementa
* Delta decrementa para iniciar reiniciar o processo

A cada 1 segundo é exibido em tela os frames objetivados.

## Graficos na Janela

Cria-se uma imagem com o tipo de colorização e tamanho.

Recebo com os graficos a imagem e caracteristicas para tudo que fizer em seguida ser para desenhar nela como formatos e colorização.

É renderizado na janela o que foi definido a partir da imagem, indicando como paramêtro a imagem a ser renderizada, offset e dimensões de altura e largura do quanto redimensionar.

BufferStrategy tem como objetivo dar conexto grafico ao objeto da classe Grafico em busca de performance gráfica.

## Animação dos Sprites

* SpriteSheet foi feito no Paint.net
* Cada posição organizada em grids para melhor posicionamento na tela a partir do código.
* Classe Spritesheet lê o sprite e armazena em buffer seu caminho.
  * O que foi feito ao instanciar a classe na variavel sheet dentro da classe Game
* Player é um vetor de Buffer que carrega em cada posição as coordenadas do sprite
  * Cada quadrado do sprite é um frame da animação

A animação foi definida pelo método Tick em curAnimation (Currenty Animation), a cada tick (a cada contagem de frame), faz uma atualização no estado da animação.
Cada estado sendo um número utilizado na posição do vetor BufferImage Player.
E assim, ao desenhar a imagem de g2 (desenho do sprite, vulgo homenzinho) o primeiro parametro correspondente ao objeto a ser desenhado será o player na posição curAnimation.

### Graphics2D e Graphics
```txt
Graphics possuem as funcionalidades de Graphics2D, mas essas foram ativadas com o Cast feito em "g".
Graphics2D é focado em funcionalidades e métodos como animações, rotações e entre outros.

O método dispose limpa os recursos gráficos das ultimas renderizações e execuções, como uma 
execução manual do Garbage Collector.
```

