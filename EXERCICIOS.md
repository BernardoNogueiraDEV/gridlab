# Respostas — CSS Grid

## 60. Container e items

O grid container é a `<section class="produtos">`, pois recebe `display: grid`.
Os grid items são os três elementos `<article>`, filhos diretos dessa seção.

## 61. Quantas colunas?

Existem três colunas. A segunda recebe a maior fração do espaço disponível.
A proporção é **1:2:1**: a segunda recebe duas partes, enquanto cada uma das
outras recebe uma parte do espaço distribuído pelas unidades `fr`.

## 62. repeat()

```css
grid-template-columns: repeat(4, 1fr);
```

## 63. Ocupação

```css
grid-column: span 2;
```

O item ocupa duas colunas a partir da posição atribuída pelo grid.

## 64. Flexbox ou Grid?

- **A — Flexbox:** os três botões são organizados em uma dimensão, na horizontal.
  `gap` pode definir espaçamento igual entre eles.
- **B — Grid:** cabeçalho, menu, conteúdo e rodapé formam um layout com relações
  entre linhas e colunas. Áreas nomeadas ajudam a visualizar essa estrutura.
- **C — Flexbox:** ícone e texto precisam de alinhamento em um único eixo,
  com `align-items: center` para centralizar no eixo transversal.
- **D — Grid:** os seis cards formam uma estrutura bidimensional de três colunas
  e duas linhas, com alinhamento entre as células.

## 65 e 66. Duas versões do dashboard

As duas seções estão em `index.html`, com estilos em `assets/css/style.css`.
Ambas usam quatro colunas equivalentes, quatro indicadores, título de largura
total, conteúdo principal em três colunas e conteúdo secundário em uma coluna.
O `gap` de 16px separa os elementos, que compartilham cores, bordas e espaçamentos.

Na primeira versão, `grid-column: 1 / -1` estende o título por toda a grade;
`1 / 4` reserva três colunas para a área principal e `4 / 5` reserva uma para
a secundária. Cada indicador usa `span 1`.

Na segunda, `grid-template-areas` desenha um mapa com as regiões `titulo`,
`vendas`, `receita`, `clientes`, `pedidos`, `principal` e `secundaria`.

**Linhas numeradas** tornam mais direto o controle de posições e extensões,
especialmente para itens repetidos ou que ocupam quantidades diferentes de colunas.
**Áreas nomeadas** tornam mais legíveis layouts com regiões semânticas estáveis,
pois o mapa mostra a organização e os nomes indicam a função de cada região.

## 67 e 68. Restrições

Os dashboards mantêm quatro colunas e não utilizam media queries, frameworks
ou Flexbox na estrutura. A adaptação completa a telas estreitas fica para o
laboratório de responsividade.
