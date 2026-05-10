# **docs/estreia-section-spec.md**

## **1) Objetivo**

A seção **Estreia / Contador** apresenta:

- uma **frase narrativa** no topo,  
- o **título do filme**,  
- o texto “ESTREIA NOS CINEMAS EM”,  
- um **contador com quatro unidades** (dias, horas, minutos, segundos),  
- a **data da estreia**,  
- e um **rodapé legal**.

A função da seção é comunicar a data de lançamento e reforçar o clima cinematográfico cósmico.

A seção **não contém**:

- botões,  
- links,  
- CTAs,  
- ícones adicionais,  
- elementos interativos além do contador,  
- ornamentos fora dos Lumas e estrelas do fundo.

---

## **2) Inventário visual (source‑of‑truth)**

### **Textos visíveis**
1. “Cada estrela guarda uma história. A sua começa agora.”  
2. “SUPER MARIO GALAXY O FILME”  
3. “ESTREIA NOS CINEMAS EM”  
4. “244”  
5. “DIAS”  
6. “10”  
7. “HORAS”  
8. “09”  
9. “MIN”  
10. “09”  
11. “SEG”  
12. “Dia 25 de Dezembro, 2025”  
13. “Super Mario Galaxy: O Filme”  
14. “Projeto conceitual para fins educacionais e ilustrativos. Nintendo, Super Mario e personagens relacionados são marcas registradas da Nintendo Co., Ltd.”

### **Elementos visuais**
1. Fundo cósmico com nebulosas (rosa, roxo, azul).  
2. Estrelas pequenas espalhadas.  
3. Lumas amarelos distribuídos no fundo.  
4. Frase superior.  
5. Título principal.  
6. Texto “ESTREIA NOS CINEMAS EM”.  
7. Contador com quatro blocos:  
   - número grande  
   - label pequeno  
8. Data da estreia.  
9. Rodapé legal em duas linhas.

### **Quantidade de elementos**
- 1 frase superior  
- 1 título  
- 1 texto auxiliar  
- 4 blocos do contador  
- 1 data  
- 1 bloco legal  
- fundo com nebulosas + estrelas + Lumas

---

## **3) Estrutura HTML (árvore + classes)**  
*(sem código, apenas estrutura conceitual)*

- `<section id="estreia" data-target-date="[DATA_DA_ESTREIA]">`  
  - container interno  
    - frase superior  
    - título  
    - texto “ESTREIA NOS CINEMAS EM”  
    - bloco do contador  
      - bloco 1  
        - número (`data-countdown="dias"`)  
        - label  
      - bloco 2  
        - número (`data-countdown="horas"`)  
        - label  
      - bloco 3  
        - número (`data-countdown="min"`)  
        - label  
      - bloco 4  
        - número (`data-countdown="seg"`)  
        - label  
    - data da estreia  
    - rodapé legal

---

## **4) Camadas visuais**

1. **Camada 0 — Fundo**  
   - nebulosas coloridas  
   - estrelas  
   - Lumas  
   - ocupa 100% da seção

2. **Camada 1 — Conteúdo textual**  
   - frase  
   - título  
   - texto auxiliar  
   - contador  
   - data  
   - rodapé legal

3. **Camada 2 — Destaque do contador**  
   - números grandes  
   - labels pequenos

---

## **5) Tokens (cores, fontes, espaçamentos, easing)**

### **Cores**
- Texto principal: `--text-primary`  
- Texto secundário / labels: `--text-muted`  
- Acentos (se necessários): `--accent-star`  
- Fundo: composição cósmica baseada em `--cosmic-purple`, `--cosmic-rose`, `--cosmic-cyan`, `--bg-mid`

### **Tipografia**
- Fonte: `--font-body`  
- Título: peso 700–900  
- Frase superior: peso médio  
- Labels do contador: caixa alta, peso 400–500  
- Rodapé legal: peso 400

### **Espaçamento**
- Padding vertical da seção: `clamp(4rem, 8vw, 6rem)`  
- Espaço entre frase e título: médio  
- Espaço entre título e texto auxiliar: pequeno  
- Espaço entre texto auxiliar e contador: médio  
- Espaço entre contador e data: médio  
- Espaço entre data e rodapé legal: pequeno

### **Motion**
- Easing padrão: `--ease-out-expo`  
- Sem animações obrigatórias no print

---

## **6) Suposições a confirmar**

- Intensidade exata do brilho das nebulosas.  
- Quantidade precisa de Lumas e estrelas.  
- Se o contador possui bordas, sombras ou separadores (não visível com clareza).  
- Distância exata entre os blocos do contador.  
- Se existe animação de entrada nos textos.  
- Se o fundo é estático ou animado.

---

## **7) Responsividade**

- Coluna única em mobile.  
- Contador deve quebrar para 2×2 se necessário.  
- Texto sempre centralizado.  
- Fundo deve manter cobertura total sem distorção.  
- Espaçamentos ajustados via `clamp()`.

---

## **8) Contrato JS (contador)**

- A seção **deve** conter:  
  `data-target-date="[DATA_DA_ESTREIA]"`

- Cada unidade do contador **deve** usar:  
  - `data-countdown="dias"`  
  - `data-countdown="horas"`  
  - `data-countdown="min"`  
  - `data-countdown="seg"`

- Valores iniciais **obrigatórios**: `"00"`

- O JS externo (não nesta etapa) irá:  
  - ler `data-target-date`  
  - calcular diferença  
  - atualizar spans  
  - nunca alterar estrutura HTML

---

## **9) Checklist de implementação**

- [ ] Usar exatamente os textos do print.  
- [ ] Usar `id="estreia"` e `data-target-date`.  
- [ ] Usar spans com `data-countdown` e valor inicial `"00"`.  
- [ ] Não adicionar elementos fora do inventário.  
- [ ] Fundo cósmico coerente com DESIGN.md.  
- [ ] Tipografia conforme tokens.  
- [ ] Labels do contador em caixa alta.  
- [ ] Layout centralizado.  
- [ ] Responsividade garantida.  
- [ ] Nenhum JS nesta etapa.  

---

## **10) Critérios de aceitação visuais**

- [ ] Fundo cósmico com nebulosas, estrelas e Lumas.  
- [ ] Frase superior centralizada.  
- [ ] Título grande e legível.  
- [ ] Texto “ESTREIA NOS CINEMAS EM” presente.  
- [ ] Contador com quatro unidades alinhadas.  
- [ ] Labels em caixa alta.  
- [ ] Data da estreia visível.  
- [ ] Rodapé legal em duas linhas.  
- [ ] Fidelidade total ao print.  

--- 