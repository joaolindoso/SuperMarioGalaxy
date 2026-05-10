# **docs/trailers-section-spec.md**

## **1) Objetivo**

A seção **Trailers** apresenta:

- um **título**,  
- um **subtítulo**,  
- e **um único player de vídeo** (embed YouTube),  

exatamente como mostrado no print.

A função da seção é exibir o trailer oficial do filme, sem interações adicionais além do próprio player.

A seção **não contém**:

- botões,  
- setas,  
- tabs,  
- carrosséis,  
- múltiplos vídeos,  
- thumbnails extras,  
- textos adicionais,  
- ícones,  
- ornamentos,  
- glows,  
- partículas.

---

## **2) Inventário visual (source‑of‑truth dos prints)**

Se não estiver aqui, **não pode aparecer no HTML**.

### **Textos visíveis**
1. **“Trailers oficiais”** — título  
2. **“Clipes da aventura no espaço.”** — subtítulo

### **Elementos visuais**
1. **Player do YouTube (iframe)**  
   - Estado: thumbnail estática  
   - Botão de play padrão do YouTube  
2. **Thumbnail do vídeo**  
   - Mostra Mario, Peach e Toad  
   - É parte do player, não um asset separado  
3. **Fundo da seção**  
   - Gradiente azul‑roxo  
4. **Espaçamentos verticais**  
   - Acima do título  
   - Entre título e subtítulo  
   - Entre subtítulo e vídeo  
   - Abaixo do vídeo

### **Quantidade de elementos**
- 1 título  
- 1 subtítulo  
- 1 vídeo  
- 1 fundo  
- 0 botões  
- 0 ícones  
- 0 elementos extras

---

## **3) Estrutura HTML (árvore + classes)**

> Estrutura mínima necessária para refletir o inventário.

- `<section id="trailers" class="trailers">`
  - `<div class="trailers__inner">`
    - `<h2 class="trailers__title">Trailers oficiais</h2>`
    - `<p class="trailers__subtitle">Clipes da aventura no espaço.</p>`
    - `<div class="trailers__video-wrapper">`
      - `<iframe src="[TRAILER_URL_1]" loading="lazy" title="Trailer oficial"></iframe>`

Nenhum outro elemento deve ser adicionado.

---

## **4) Camadas visuais**

1. **Camada 0 — Fundo**  
   - Gradiente azul‑roxo  
   - Preenche toda a seção

2. **Camada 1 — Textos**  
   - Título acima  
   - Subtítulo logo abaixo  
   - Ambos centralizados

3. **Camada 2 — Player de vídeo**  
   - Centralizado  
   - Ocupa a maior parte da largura  
   - Mantém proporção 16:9

---

## **5) Tokens (cores, fontes, espaçamentos, easing)**

### **Cores**
- Título: `--text-primary`  
- Subtítulo: `--text-muted`  
- Fundo: gradiente coerente com DESIGN.md (Cosmic Purple + Cosmic Cyan + Cosmic Rose)  
- Player: padrão do YouTube (não estilizado)

### **Tipografia**
- Título:  
  - `--font-body`  
  - Peso 700–900  
  - Tamanho aproximado: display médio (equivalente a `--font-size-4xl` do sistema anterior)

- Subtítulo:  
  - `--font-body`  
  - Peso 400–500  
  - Tamanho aproximado: `--font-size-lg`

### **Espaçamento**
- Padding vertical: `clamp(4rem, 8vw, 6rem)`  
- Espaço entre título e subtítulo: `var(--space-3)`  
- Espaço entre subtítulo e vídeo: `var(--space-8)`  

### **Motion**
- Nenhuma animação além do player  
- Easing padrão do sistema: `--ease-out-expo`

---

## **6) Suposições a confirmar**

- Intensidade exata do gradiente azul‑roxo (print não mostra valores precisos).  
- Se o player possui bordas arredondadas (parece ter, mas não é 100% claro).  
- Se existe sombra leve ao redor do vídeo (não confirmável pelo print).  
- Margens exatas acima e abaixo do vídeo.  

---

## **7) Responsividade**

- Player deve manter proporção 16:9 usando wrapper.  
- Título e subtítulo centralizados em todas as larguras.  
- Padding lateral reduzido em telas pequenas.  
- Vídeo ocupa 100% da largura disponível até o limite do container.  
- Nenhum elemento deve quebrar linha de forma inesperada.

---

## **8) Estados**

### **Visíveis no print**
- Player em estado estático (thumbnail).  
- Botão de play padrão do YouTube.  

### **Não visíveis (portanto não implementar)**
- Hover customizado  
- Overlays  
- Controles estilizados  
- Animações de entrada  
- Carrosséis  
- Tabs  
- Múltiplos vídeos  

---

## **9) Checklist de implementação**

- [ ] Usar **exatamente** os textos do print.  
- [ ] Usar **exatamente** 1 vídeo.  
- [ ] Usar `<iframe>` com `loading="lazy"` e `title` descritivo.  
- [ ] Não adicionar botões, CTAs ou links externos.  
- [ ] Não adicionar ícones ou ornamentos.  
- [ ] Fundo com gradiente azul‑roxo coerente com DESIGN.md.  
- [ ] Player centralizado e responsivo.  
- [ ] Nenhum elemento além dos listados no inventário.  
- [ ] Não estilizar o player além do necessário para responsividade.  

---

## **10) Critérios de aceitação visuais**

- [ ] Título e subtítulo idênticos ao print.  
- [ ] Player único, centralizado, com thumbnail visível.  
- [ ] Fundo azul‑roxo cobrindo toda a seção.  
- [ ] Espaçamentos coerentes com o print.  
- [ ] Nenhum elemento extra.  
- [ ] Layout limpo e direto.  
- [ ] Proporção 16:9 preservada.  
- [ ] Fidelidade total ao print.  

---
