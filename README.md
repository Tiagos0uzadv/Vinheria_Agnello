# Vinheria Angnello

Site institucional da Vinheria Angnello, uma vinheria familiar fictícia. O caso apresenta uma vinícola fundada em 1978 por Giovanni Angnello, filho de imigrantes italianos, que hoje é conduzida pela terceira geração da família. O site apresenta os rótulos, conta a história da vinícola, exibe uma galeria de vinhos e oferece um canal de contato.

No Check-Point 02 o projeto recebeu um incremento visual com pseudo-classes, pseudo-elementos, animações, transições e transformações em CSS.

## Estrutura do projeto

```
Vinheria_Agnello/
├── index.html
├── README.md
└── src/
    ├── assets/
    │   └── imgs/           → logotipos e fotos dos rótulos
    ├── css/
    │   ├── style.css       → estilos base (layout, cores, tipografia, responsividade)
    │   └── efeitos.css     → efeitos visuais do CP2 (importado pelo style.css)
    └── pages/
        ├── historia.html
        ├── galeria.html
        └── contato.html
```

- `index.html`: página inicial com o cardápio de vinhos, um resumo da história e os contatos.
- `src/pages/historia.html`: história e tradição da família Angnello.
- `src/pages/galeria.html`: galeria com as fotos dos rótulos.
- `src/pages/contato.html`: formulário de contato e outros canais de atendimento.

## Integrantes

- Tiago Souza
- Cauã Almeida Moura
- Felipe Fontes

## Site publicado

GitHub Pages: https://tiagos0uzadv.github.io/Vinheria_Agnello/

## Efeitos Visuais

Todos os efeitos ficam em `src/css/efeitos.css`, que é importado pelo `style.css` com `@import url("efeitos.css");`.

### Pseudo-classes

| Pseudo-classe | Onde é usada | Efeito |
| --- | --- | --- |
| `:hover` | links do menu, logo, cartões de vinho, figuras da galeria, imagem da história, links e botão | realça cor, sombra e posição do elemento |
| `:focus` / `:focus-visible` | links do menu, botão e campos do formulário | contorno dourado na navegação por teclado e brilho no campo ativo |
| `:active` | botão "Enviar mensagem" | o botão encolhe levemente ao ser clicado |
| `:checked` | menu mobile (checkbox escondido) | abre o menu e transforma o ícone "hambúrguer" em um X |
| `:nth-child()` | figuras da galeria e cartões de vinho | atrasa a animação de entrada de forma alternada/em sequência |
| `:not()` | parágrafos das seções | ajusta o espaçamento de todos os parágrafos, menos o último |
| `:target` | seção de vinhos | anima os cartões ao clicar em "Vinhos" no menu |
| `:user-invalid` | campos do formulário | borda vermelha quando o usuário preenche um campo de forma inválida |

### Pseudo-elementos

| Pseudo-elemento | Onde é usado | Efeito |
| --- | --- | --- |
| `::before` | títulos das seções (`h2`) | marcador ornamental "•" girado com `rotate()` |
| `::before` | tipo do vinho nos cartões | losango decorativo "◆" |
| `::before` / `::after` | ícone do menu mobile | as duas barras do "hambúrguer", que giram e formam um X |
| `::after` | cabeçalho das páginas internas | filete dourado animado abaixo do título |
| `::first-letter` | primeiro parágrafo dos textos de história | letra capitular dourada e maior |
| `::selection` | todo o site | texto selecionado em dourado com letra vinho |
| `::placeholder` | campos do formulário | placeholder em itálico e em tom mais suave |

### Animações (`@keyframes`)

- `page-arrive`: o conteúdo (blocos de texto, figuras e cartões) aparece subindo e ganhando opacidade.
- `accent-grow`: o filete dourado do cabeçalho cresce a partir do centro (`scaleX`).
- `fade-down`: os títulos e o menu mobile aberto descem suavemente ao aparecer.
- `logo-float`: o logo "flutua" devagar, com leve inclinação, em loop infinito.

### Transições e transformações

- **Transições:** cor de fundo e posição dos links do menu, sombra e posição dos cartões e figuras, zoom das imagens, cor e borda dos campos do formulário, cor e posição do botão, sublinhado dos links e rotação do ícone do menu.
- **`translateY()`:** links do menu, cartões, figuras e botão sobem alguns pixels no hover.
- **`scale()`:** zoom nas imagens dos cartões, da galeria e da história; o botão encolhe no clique.
- **`rotate()`:** leve giro nas imagens da galeria, no marcador dos títulos, no logo e no ícone do menu (que vira X).
- **`scaleX()`:** crescimento do filete decorativo do cabeçalho.

### Acessibilidade

Quando o sistema operacional pede menos movimento (`prefers-reduced-motion: reduce`), as animações e transições são praticamente desligadas.
