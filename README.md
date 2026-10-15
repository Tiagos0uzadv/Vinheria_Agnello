# Vinheria Angnello

Site institucional de uma vinheria familiar fictícia, com páginas para apresentar os rótulos, contar a história da vinícola, exibir uma galeria e oferecer contato.

## Estrutura do projeto

- `index.html`: página inicial e seleção de vinhos.
- `historia.html`: história e tradição familiar.
- `galeria.html`: galeria de rótulos.
- `contato.html`: formulário e dados de contato.
- `styles.css`: estilos base compartilhados.
- `efeitos.css`: interações, animações e detalhes decorativos compartilhados.
- `photos/`: logotipos e imagens dos rótulos.

## Integrantes

Nomes não informados no material do projeto. Preencher com os integrantes do grupo.

## Site publicado

GitHub Pages: publicação ainda não identificada. Após publicar, inserir aqui o endereço do site.

## Efeitos Visuais

- **Pseudo-classes:** `:hover` realça links, imagens e botões; `:focus-visible` destaca a navegação por teclado e os controles; `:nth-child(even)` aplica atraso alternado às figuras da galeria; `:not(:last-child)` ajusta o espaçamento dos parágrafos.
- **Pseudo-elementos:** `::after` cria o filete decorativo animado nos cabeçalhos; `::before` acrescenta um marcador ornamental aos títulos das seções.
- **Animações:** `@keyframes page-arrive` revela o conteúdo com deslocamento e opacidade; `@keyframes accent-grow` expande o filete dos cabeçalhos.
- **Transições e transformações:** links, cartões, imagens, campos e botão suavizam as mudanças de estado. Há deslocamentos com `translateY()`, ampliação com `scale()` e leve rotação com `rotate()` nas imagens da galeria.
- **Acessibilidade:** os efeitos de movimento são reduzidos quando o sistema solicita `prefers-reduced-motion`.