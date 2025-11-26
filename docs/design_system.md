# Design System do Dashboard de Vendas do Xbox

Um **Design System** é um conjunto de regras visuais e funcionais que garante consistência e clareza em dashboards e relatórios.  
Neste projeto, o design foi inspirado na identidade visual do Xbox.

---

## Paleta de Cores
- **Xbox Green:** `#9BC848` — cor principal para destaques e títulos.
- **Secondary Green:** `#22C55E` — usada em gráficos positivos e indicadores.
- **Aqua Accent:** `#2AE6B1` — cor de apoio para diferenciação de categorias.
- **Menu Green:** `#5BF6A8` — aplicada em filtros visuais (Slicers).
- **Neutral Gray:** `#E8E6E9` — fundo neutro para áreas de respiro e cartões.

---

## Tipografia
- **Fonte padrão:** Calibri (Excel default).
- **Títulos:** negrito, tamanho 16–20 pt.
- **Rótulos de gráficos:** tamanho 10–12 pt, sempre legíveis.
- **Big Numbers:** tamanho 24–28 pt, em verde principal.

---

## Layout do Dashboard
- **Topo:** título principal “XBOX GAME PASS SUBSCRIPTIONS SALES”.
- **Linha 1:** filtros visuais (Slicers) organizados horizontalmente.
- **Linha 2:** cards de Big Numbers:
  - Faturamento Anual.
  - Auto-renovação Yes vs No.
  - EA Play total.
  - Minecraft total.
- **Linha 3:** gráficos dinâmicos (colunas, barras, pizza).
- **Rodapé:** notas de contexto (“Info Context”).

---

## Gráficos e Visualizações
- **Big Numbers:** caixas de texto vinculadas a métricas (SUMIFS ou Pivot).
- **Gráficos de barras:** comparação Yes vs No (auto-renovação).
- **Gráficos de colunas:** distribuição por plano (Core, Standard, Ultimate).
- **Gráficos de pizza:** proporção de vendas de add-ons (EA Play, Minecraft).
- **Filtros (Slicers):** Plan, Auto Renewal, Subscription Type, Month.

---

## Princípios de Design
1. **Clareza:** cada gráfico responde a uma pergunta de negócio.
2. **Consistência:** cores e fontes aplicadas de forma uniforme.
3. **Interatividade:** uso de Slicers para permitir exploração dos dados.
4. **Minimalismo:** evitar elementos desnecessários (linhas de grade, legendas redundantes).
5. **Contexto:** cada Big Number acompanhado de uma nota explicativa.

---

## Info Context
- **Exemplo:** abaixo do número de faturamento anual, incluir “Somente planos Annual”.
- **Objetivo:** evitar interpretações erradas e dar transparência ao cálculo.

---

## Conclusão
O Design System garante que o dashboard:
- Seja **visualmente atraente**.
- Tenha **consistência** em cores, fontes e layout.
- Permita **análise rápida** e **decisões seguras**.
- Reforce a identidade visual do Xbox.

Este documento serve como guia para futuras evoluções do dashboard e para manter a qualidade visual em novos projetos. 

