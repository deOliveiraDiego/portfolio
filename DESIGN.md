---
name: Diego de Oliveira · Product Builder
description: Portfólio de uma página em que cada afirmação traz uma prova que dá para abrir agora.
colors:
  paper: "#F6F5F1"
  surface: "#FFFFFF"
  ink: "#15171C"
  ink-2: "#4A4E57"
  ink-3: "#6B6F78"
  rule: "#E2E0D9"
  proof-blue: "#2447D6"
  proof-blue-soft: "rgba(36, 71, 214, .08)"
  bar-old: "#C9C6BC"
  paper-dark: "#111317"
  surface-dark: "#181B20"
  ink-dark: "#EDEBE6"
  ink-2-dark: "#B4B2AC"
  ink-3-dark: "#8E8C87"
  rule-dark: "#2A2D33"
  proof-blue-dark: "#8FA6FF"
typography:
  display:
    fontFamily: "Schibsted Grotesk, system-ui, sans-serif"
    fontSize: "clamp(44px, 7.4vw, 88px)"
    fontWeight: 600
    lineHeight: 0.98
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Schibsted Grotesk, system-ui, sans-serif"
    fontSize: "clamp(32px, 4.4vw, 52px)"
    fontWeight: 600
    lineHeight: 1.04
    letterSpacing: "-0.03em"
  title:
    fontFamily: "Schibsted Grotesk, system-ui, sans-serif"
    fontSize: "19px"
    fontWeight: 600
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Schibsted Grotesk, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Schibsted Grotesk, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
  numeral:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: "14px"
    fontWeight: 400
    letterSpacing: "-0.01em"
    fontFeature: "tnum"
rounded:
  bar: "6px"
  frame: "14px"
  pill: "999px"
spacing:
  gutter-mobile: "16px"
  gutter: "24px"
  row: "20px"
  block: "48px"
  container: "1120px"
components:
  chip:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    height: "40px"
    padding: "0 16px"
  chip-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    height: "40px"
    padding: "0 16px"
  chip-primary-hover:
    backgroundColor: "{colors.proof-blue}"
    textColor: "{colors.paper}"
  proof-link:
    textColor: "{colors.proof-blue}"
    typography: "{typography.body}"
  frame:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.frame}"
  measure-panel:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.frame}"
    padding: "32px"
  index-row:
    textColor: "{colors.ink}"
    padding: "20px 0"
---

# Design System: Diego de Oliveira · Product Builder

## Overview

**Creative North Star: "The Verifiable Ledger"**

Um portfólio clássico de builder, calmo e editorial: papel quente, tinta quase preta, réguas finas e uma única cor que significa "isso você pode conferir agora". A página é um índice seguido de casos; cada caso é título, quadro de tela, texto em duas colunas e uma ficha de fatos. O enquadramento some para o trabalho aparecer.

A densidade é baixa e o ritmo é vertical: grandes respiros entre casos (80 a 136px), réguas de 1px organizando listas no lugar de caixas. Profundidade existe só nos objetos de prova (quadros de tela e o painel de medição), nunca no layout.

**Key Characteristics:**
- Fundo de papel quente com tinta neutra; um só acento.
- Números sempre em mono tabular.
- Listas e fichas feitas de réguas finas, não de cards.
- Todas as capturas no mesmo quadro, mesma proporção (16:10) e mesmo raio.
- Tema escuro espelhado por token, sem mudar estrutura.

## Colors

Neutros quentes de papel e tinta, com um azul-tinta reservado para provas e interação.

### Primary
- **Proof Blue** (`proof-blue`): links de prova ("Abrir a demo", "Código", "Medir…"), o marcador "demo ao vivo" no índice, a barra do resultado novo e o valor em destaque do comparativo. Também é o estado de hover do contato principal e do e-mail final, o anel de foco e a seleção de texto. No escuro vira `proof-blue-dark`.
- **Proof Blue Soft** (`proof-blue-soft`): trilho das barras de medição.

### Neutral
- **Warm Paper** (`paper`): fundo da página.
- **Surface White** (`surface`): interior de chips, quadros e painel de medição.
- **Ink** (`ink`): títulos, texto principal, chip principal em repouso.
- **Ink 2** (`ink-2`): texto corrido e lede.
- **Ink 3** (`ink-3`): rótulos, legendas, contexto, rodapé, seta do índice.
- **Hairline** (`rule`): todas as réguas e contornos de 1px.
- **Old Bar** (`bar-old`): a barra do "antes" no comparativo; neutra de propósito.

### Named Rules
**The One Proof Color Rule.** O azul só aparece em algo clicável que leva a uma prova, no dado novo que a prova mede, ou como estado de interação. Texto decorativo, títulos e ícones em repouso nunca são azuis.

**The Neutral Before Rule.** Em comparações, o "antes" é cinza-papel e o "depois" é azul; nunca vermelho contra verde.

## Typography

**Display/Body Font:** Schibsted Grotesk (com system-ui)
**Numeral Font:** JetBrains Mono (com ui-monospace)

**Character:** Um grotesco firme e sem afetação para tudo que é texto; mono tabular para tudo que é número ou stack, para que dados pareçam medidos, não escritos.

### Hierarchy
- **Display** (600, clamp 44–88px, 0.98, -0.035em): só o nome no topo.
- **Headline** (600, clamp 32–52px, 1.04, -0.03em): título de cada caso. Versão menor (clamp 24–30px) nas seções quietas; o fecho usa clamp 28–64px em `ink-3` com o e-mail em `ink`.
- **Title** (600, 18–20px, -0.01em): nomes no índice, h3 do painel e dos itens.
- **Body** (400, 17px, 1.6): texto corrido, máximo 62ch; lede em 18–21px, 1.5, máximo 34ch.
- **Label** (400–500, 13–15px): fichas, legendas (14px), contexto, chips.
- **Numeral** (mono 400–500, 14–20px, tabular): métricas do índice, valores do comparativo, stacks e fatos numéricos das fichas.

### Named Rules
**The Mono Numbers Rule.** Todo número que é evidência (tempo, nota, contagem de testes) vai em mono tabular. Texto nunca vai em mono.

## Layout

Coluna única centrada em `min(1120px, 100% - 48px)`; abaixo de 820px o gutter cai para 16px de cada lado. O topo é grade de duas colunas (texto à esquerda, retrato à direita alinhado à base); o índice é grade de quatro colunas (nome 300px, descrição, métrica 150px à direita, seta). Cada caso: cabeçalho 2fr/1fr com o contexto alinhado à direita, figura em largura total, corpo em duas colunas iguais com gap de 48px. Seções quietas usam 1fr/2fr com régua no topo.

Ritmo: 48px entre blocos, 20–24px entre elementos, 80–136px entre casos. Em 820px tudo colapsa para uma coluna, o retrato sobe para 112px acima do nome, a seta do índice some e a métrica sobe para a primeira linha. Em 480px o chip de e-mail ocupa a largura toda.

## Elevation & Depth

Híbrido contido: o layout é plano e separado por réguas; só objetos de prova recebem sombra ambiente mais um contorno interno de 1px em `rule`.

### Shadow Vocabulary
- **Proof lift** (`0 1px 2px rgba(21,23,28,.04), 0 8px 24px -12px rgba(21,23,28,.14)`; escuro `0 1px 2px rgba(0,0,0,.3), 0 8px 24px -12px rgba(0,0,0,.5)`): quadros de tela, painel de medição e retrato.

### Named Rules
**The Lift Is Evidence Rule.** Se um elemento tem sombra, ele é uma captura ou uma medição. Listas, fichas, índice e texto ficam planos.

## Shapes

Três raios: 14px para quadros, painel e retrato; 6px para barras; pílula (999px) para chips. Réguas de 1px em `rule` são a forma dominante: topo e base de cada linha do índice e da ficha, rodapé, topo das seções quietas. Capturas são cortadas em 16:10 ancoradas no topo; a captura de celular ao lado estica para a altura do par.

## Components

### Buttons (chips de contato)
- **Shape:** pílula (999px), 40px de altura, 0 16px, 15px/500, ícone de 16px.
- **Default:** fundo `surface`, régua `rule`; hover escurece a régua para `ink`.
- **Primary:** fundo e régua `ink`, texto `paper`; hover vira `proof-blue`.
- **Focus:** anel de 2px `proof-blue`, offset 4px, em todos os links.

### Proof links
Texto `proof-blue` 500, 15–16px, com seta diagonal de 14px. Hover sublinha (1px, offset 4px) e a seta anda 2px para cima e para a direita. Agrupados em linha com gap 8px 24px.

### Index rows
Linha inteira clicável entre réguas, 20px de padding vertical. Nome em title, descrição em `ink-3`, métrica em mono `ink` à direita (ou "demo ao vivo" em `proof-blue` quando a prova é ao vivo). Hover desloca o nome 6px à direita e a seta desce 2px e fica azul.

### Frames (quadros de tela)
Raio 14px, fundo `surface`, proof lift, contorno interno de 1px. Legenda abaixo em 14px `ink-3`, 12px de margem.

### Fact sheet (ficha)
Lista de pares rótulo/valor entre réguas, 14px de padding vertical, 15px; rótulo em `ink-3` à esquerda, valor à direita.

### Measure panel (comparativo)
Card `surface` de 32px (20px no mobile) com proof lift. Cada linha: rótulo com nota em 13px, trilho de 28px em `proof-blue-soft`, valor em mono 20px. As barras crescem da esquerda em 1.4s (`cubic-bezier(.16,1,.3,1)`) quando o painel entra em vista, a nova com 0.25s de atraso; com movimento reduzido ficam estáticas. Rodapé com régua, nota metodológica e os dois links de prova.

## Do's and Don'ts

### Do:
- **Do** colocar ao lado de cada afirmação um link de prova em `proof-blue`.
- **Do** escrever números de evidência em JetBrains Mono tabular.
- **Do** separar listas com réguas de 1px `rule`, não com cards.
- **Do** mostrar toda captura no quadro de 14px, 16:10, com proof lift.
- **Do** usar a mesma curva `cubic-bezier(.16,1,.3,1)` em toda transição e respeitar `prefers-reduced-motion`.

### Don't:
- **Don't** usar o azul em títulos, texto decorativo ou ícones em repouso.
- **Don't** pôr sombra em listas, fichas ou blocos de texto.
- **Don't** usar vermelho/verde em comparativos; o "antes" é `bar-old`.
- **Don't** introduzir um segundo acento ou um terceiro tom de fundo além de `paper` e `surface`.
- **Don't** colocar rótulos sobre os títulos (kickers/eyebrows); o título abre a seção direto.
