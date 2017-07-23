---
layout: post
title: Como instalar SDL2, SDL2_image, SDL2_ttf e SDL2_mixer no Linux Debian/Ubuntu
---

Quando comecei com o *desenvolvimento de jogos* usando *SDL2*, uma das minhas maiores dificuldades era instalar a *lib de desenvolvimento* no *Linux*, já que a maioria dos tutoriais usavam *Windows*, tive que passa um bom tempo dando uma bela procurada no nosso querido *Stack Overflow*, logo resolvi criar este guia para agilizar as coisas.

## Instalando o SDL2(Simple DirectMedia Layer 2.0)

"SDL2.h" é o header fundamental para todas as aplicações com SDL

Abra o terminal e escreva os comandos:

```
sudo apt-get update
sudo apt-get install libsdl2-dev
```

## Instalando libs adicionais:

Além da lib principal, há também outras libs que auxiliam o desenvolvimento, veja uma descrição breve de cada uma e como instala-las:

### SDL2_image

Permite carregar arquivos de imagem como JPG e PNG.
```
sudo apt-get update
sudo apt-get install libsdl2_image-dev</addr>
```

### SDL2_mixer

Permite carregar arquivos de audio.
```
sudo apt-get update
sudo apt-get install libsdl2_mixer-dev
```

### SDL2_ttf

Permite carregar fontes e gerar textos.
```
sudo apt-get update
sudo apt-get install libsdl2_ttf-dev
```

## Incluir em arquivos C/C++

```c++
#include <SDL2/SDL.h>
#include <SDL2/SDL_image.h>
#include <SDL2/SDL_ttf.h>
#include <SDL2/SDL_mixer.h>
```

## Link no compilador g++

Utilizando o compilador g++ com as flags de cada lib:
```
g++ seu_arquivo.cpp -o nome_do_executavel -lSDL2 -lSDL2_image -lSDL2_ttf -lSDL2_mixer
```


Qualquer dúvida, contacte-me e tentarei lhe ajudar, boa sorte!

