---
layout: post
title: Incapaz de criar contexto - SDL2 e OpenGLtags:
- glew
- gl
- lib
- opengl
- sdl2
- sdl
- context
- c
- c++
- cpp
- c/c++
- c/cpp
- code
---

Se tem algo que eu sou profissional, este algo é cometer erros por falta de atenção. Foi o que aconteceu, passei um tempo tentando entender porquê não consegui passar o contexto OpenGL para minha janela SDL_Window, e a solução foi bem simples.

O problema foi ter esquecido a flag **SDL_WINDOW_OPENGL** na criação da janela *SDL_Window*.
```
SDL_Window *window = SDL_CreateWindow("title", x, y, w, h, **SDL_WINDOW_OPENGL**);
```
Esta flag diz a função *SDL_CreateWindow* que ela deve ter suporte a OpenGL, permitindo que você crie o contexo;
*Caso queira adicionar mais flags, use o operador bitwise or(|)*

### Contribua com o site!
Caso tenha alguma dúvida(ou solução), entre em contato, ficarei grato em postar a solução assim que possível.
