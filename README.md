# ATIVIDADE RAYCAST
Este projeto é uma cena feita com o Unity 3D utilizando Raycast e o conceito Destroy e a mecânica de Prefabs da engine.

## AUTORES
Gustavo Henrique Moraes Rocillo e Yuri Telis Garcia.

## DETALHES DO PROCESSO DE DESENVOLVIMENTO
Para início, a cena no Unity foi criada e começou o planejamento do que iria ser feito, o que resultou em um tiro ao alvo onde os alvos eram "Dummies". Na Asset Store do Unity, foram escolhidos tanto o pacote com o dummy quanto um pacote para os objetos do cenário (links no final do Readme) e foram colocados na cena.
<br>
Em seguida, foi iniciado o processo de programação, iniciado com o script de movimentação da câmera e o de travar o cursor na tela e logo o script do Raycast, sendo todos adicionados à câmera principal do projeto.

## SCRIPTS DO PROJETO
Script para a movimentação da câmera:
<br> <img src="img/script cam 1.jpg">
<img src="img/script cam 2.jpg"> <br>
EXPLICAÇÃO: <br>
O código permite a rotação da câmera usando o mouse. Ele oferece opções para rotação nos eixos X e Y, com sensibilidades ajustáveis e limites de rotação vertical definidos. A câmera é rotacionada de acordo com os movimentos do mouse, proporcionando uma interação dinâmica com o ambiente do jogo.

Script para travar o cursor na tela:
<br> <img src="img/script cursor.jpg"> <br>
EXPLICAÇÃO: <br>
Quando definimos Cursor.lockState para CursorLockMode.Locked, estamos essencialmente "travando" o cursor do mouse dentro da janela do jogo ou aplicativo. Isso significa que o cursor não será visível e não poderá sair da área da janela, mesmo que o usuário mova o mouse fora dessa área.

Script do Raycast com o conceito de Destroy:
<br> <img src="img/script raycast 1.jpg">
<img src="img/script raycast 2.jpg"> <br>
EXPLICAÇÃO: <br>
Este código pode ser dividido em duas partes
Spawnar Prefab: O método SpawnarPrefab() é chamado no início do jogo e continua a instanciar objetos em posições aleatórias dentro de determinados limites de coordenadas a cada 3 segundos.
<br>
Raycasting: O método Update() verifica se o botão esquerdo do mouse foi clicado, se sim, um raio é lançado a partir da posição da câmera na direção do ponteiro do mouse, se esse raio atingir um objeto no jogo, e esse objeto for marcado com a tag "alvo", então ele é destruído e um contador de alvos destruídos é incrementado, fazendo com que, a UI de texto exibe o número atual de alvos destruídos.

## IMAGEM DO PROJETO
A tela do projeto assim que o abre:
<br> <img src="img/tela inicial.jpg">

## LINKS
### PROJETO
Cena: https://drive.google.com/file/d/1UdbuoJFGL2qT1awD00kkdA3IZL8OvBIT/view?usp=drive_link

Vídeo da cena: https://drive.google.com/file/d/18G7qDXfeclBzr2SSCAXZZeha1YCfcqUw/view?usp=sharing

### ASSETS
Alvos: https://assetstore.unity.com/packages/3d/props/lowpoly-training-dummy-202311

Cenáro: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153