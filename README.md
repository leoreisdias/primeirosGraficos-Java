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