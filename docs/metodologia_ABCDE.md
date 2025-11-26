# Metodologia ABCDE aplicada ao Dashboard de Vendas do Xbox

A metodologia **ABCDE** é um framework simples e poderoso para estruturar projetos de análise de dados e dashboards.  
Ela garante que o processo seja organizado, lógico e focado em resultados de negócio.

---

## A — Avaliar
- **Objetivo:** entender o problema de negócio e definir as perguntas que precisam ser respondidas.
- **No projeto:** identificar métricas críticas de vendas do Xbox Game Pass:
  - Faturamento total de planos anuais.
  - Faturamento anual separado por auto-renovação (Yes/No).
  - Total de vendas do EA Play Season Pass.
  - Total de vendas do Minecraft Season Pass.
- **Resultado esperado:** clareza sobre o que medir e como apresentar.

---

## B — Base
- **Objetivo:** conhecer e organizar os dados brutos.
- **No projeto:** utilizar o arquivo `data/base01.xlsx`, que contém:
  - Informações de assinantes (ID, Nome, Plano, Data de início).
  - Tipo de assinatura (Monthly, Quarterly, Annual).
  - Preços e valores totais.
  - Flags de auto-renovação e Season Pass.
- **Resultado esperado:** base limpa, normalizada e pronta para análise.

---

## C — Calcular
- **Objetivo:** transformar dados em métricas e indicadores.
- **No projeto:** aplicar fórmulas e tabelas dinâmicas para calcular:
  - Soma de `Total Value` para planos anuais.
  - Soma de `Total Value` por auto-renovação.
  - Soma de `EA Play Season Pass Price` quando ativo.
  - Soma de `Minecraft Season Pass Price` quando ativo.
- **Ferramentas usadas:** funções `SUMIFS`, tabelas dinâmicas, colunas auxiliares (Month, Has Coupon).
- **Resultado esperado:** métricas confiáveis e replicáveis.

---

## D — Design
- **Objetivo:** transformar métricas em visualizações claras e atraentes.
- **No projeto:**
  - Uso de paleta de cores oficial do Xbox.
  - Criação de gráficos dinâmicos (colunas, barras, pizza).
  - Inserção de Slicers (filtros visuais) para interação.
  - Organização em cards de Big Numbers e gráficos complementares.
- **Resultado esperado:** dashboard visualmente consistente e intuitivo.

---

## E — Entregar
- **Objetivo:** disponibilizar o dashboard final e documentar o processo.
- **No projeto:**
  - Arquivo final `dashboards/dashboard_xbox_finalizado01.xlsx`.
  - Documentação em `README.md`, `metodologia_ABCDE.md` e `designsystem.md`.
  - Capturas de tela em `docs/capturas/`.
- **Resultado esperado:** entrega profissional, reprodutível e bem documentada.

---

## Conclusão
A metodologia **ABCDE** garante que o projeto seja:
- **Estruturado** (cada etapa tem um propósito).
- **Didático** (fácil de entender e reproduzir).
- **Orientado a negócio** (responde perguntas reais).
- **Visualmente claro** (design consistente).
- **Entregável** (documentação e arquivos organizados).

Este framework pode ser aplicado a qualquer projeto de análise de dados, não apenas ao Xbox Game Pass. 

