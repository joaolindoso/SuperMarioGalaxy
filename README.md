# Super Mário Galaxy

## ✨ Sobre o Projeto  
Trata-se de projeto inspirado no universo de **Super Mario Galaxy**, com foco em atmosfera cósmica, contraste cinematográfico e tokens visuais fiéis ao tema.  

---

## 🛠️ Tecnologias Utilizadas  
Este projeto foi desenvolvido com foco educacional, utilizando:

- **HTML5**  
- **CSS3**  
- **JavaScript**  
- **GSAP (GreenSock Animation Platform)** — animações e microinterações  
- **VS Code**  
- **Microsoft Copilot Pro**

---

## 🌠 1. Visual Theme & Atmosphere  
Um sistema cinematográfico com atmosfera cósmica, contraste alto e brilho controlado.  
A interface prioriza legibilidade em fundo profundo, com acentos estelares para orientar foco narrativo e ação.

- **Density:** 5/10  
- **Variance:** 6/10  
- **Motion:** 6/10  

---

#🌌 Design System

## 🎨 2. Color Palette & Roles  
- **Cosmic Deep** (`#000000`) — Fundo base global  
- **Cosmic Mid** (`#0a0a1a`) — Fundo intermediário  
- **Cosmic Surface** (`#141340`) — Superfícies de componentes  
- **Starlight Primary** (`#f5f0e8`) — Texto principal  
- **Starlight Muted** (`rgba(245, 240, 232, 0.72)`) — Texto secundário  
- **Power Star** (`#ffd23f`) — Accent principal  
- **Power Star Dim** (`rgba(255, 210, 63, 0.12)`) — Pills e hovers  
- **Cosmic Cyan** (`#5ce0d8`) — Destaques e glows  
- **Cosmic Purple** (`#6a3cbc`) — CTA secundário  
- **Cosmic Rose** (`#c8508c`) — Acento narrativo  

---

## 🔤 3. Typography Rules  
- Fonte principal: **Outfit, sans-serif**  
- Hierarquia: títulos 700–900; corpo 400–500  
- Ritmo de leitura: entrelinha confortável, largura 55–70 caracteres  
- Labels utilitários em caixa alta com leve espaçamento  
- Fallback: `sans-serif`

---

## 🧩 4. Component Stylings  
- **Buttons:** Primário em Power Star; secundário em Cosmic Purple  
- **Cards:** Base em Cosmic Surface, contraste tonal  
- **Countdown/Metrics:** Dígitos destacados  
- **Badges/Pills:** Fundo Power Star Dim  
- **Hero:** Composição espacial de alto impacto  

---

## 📐 5. Layout Principles  
- Grid-first com alinhamento consistente  
- Largura máxima entre 1200–1400px  
- Assimetria permitida em hero e blocos editoriais  
- Mobile (<768px): coluna única  
- Espaçamento fluido via `clamp(...)`

---

## 🎞️ 6. Motion & Interaction  
- **Easings principais:**  
  - `--ease-out-expo`  
  - `--ease-spring`  
- Entradas em cascata  
- Microinterações por opacidade e deslocamento  
- Animações otimizadas em `transform` e `opacity`  
- GSAP aplicado para fluidez e controle avançado  

---

## 🚫 7. Anti-Patterns (Banned)  
- Não usar paleta inferida por screenshot  
- Não substituir Outfit por Inter  
- Não usar branco puro como texto padrão  
- Não introduzir cinzas fora da paleta  
- Não aplicar glow externo agressivo  
- Não criar gradientes fora do conjunto oficial  

---

## 🧪 8. Canonical Token Snippet  
```css
:root {
  --bg-deep: #000000;
  --bg-mid: #0a0a1a;
  --bg-surface: #141340;
  --text-primary: #f5f0e8;
  --text-muted: rgba(245, 240, 232, 0.72);
  --accent-star: #ffd23f;
  --accent-star-dim: rgba(255, 210, 63, 0.12);
  --cosmic-cyan: #5ce0d8;
  --cosmic-purple: #6a3cbc;
  --cosmic-rose: #c8508c;
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
  --font-body: 'Outfit', sans-serif;
}
```

---

## 🚀 Como Executar o Projeto  
1. Clone o repositório:  
   ```bash
   git clone https://github.com/seu-usuario/super-mario-galaxy-design-system.git
   ```
2. Abra o diretório no VS Code  
3. Inicie um servidor local (ex.: Live Server)  
4. Acesse no navegador:  
   ```
   http://localhost:5500
   ```

---

## 📩 Contato  
Para dúvidas, sugestões ou melhorias, abra uma *issue* ou envie um *pull request*.

---
