# Desafio GO

Projeto destinado a atender ao desafio 1 do módulo Docker do curso FullCycle 3.0.


O projeto foi criado utilizando a linguagem de programação GO e foi compilado utilizando a imagem golang do docker.


Foi utilizado o recurso multistage, do docker, para realizar a compilação do projeto e, posteriormente, copiá-lo para uma imagem menor para ser executado.


O resultado esperado é que seja impresso no console a frase "Full Cycle Rocks!""


[Link da imagem](https://hub.docker.com/r/brcgimenez/fullcycle) disponível no Docker HUB.


Para executar a imagem, far-se-a necessário executar o comando:

`docker run -it brcgimenez/fullcycle:1.0`