# Criando um Dashboard de Vendas do Xbox com Excel

![CienciaDadosSantander](https://github.com/user-attachments/assets/024c95b3-0def-4b69-9c61-fccfc0403732)

**Bootcamp Santander 2025 - Ciência de Dados com Python**

---

**DESCRIÇÃO:**
Aprenda a criar um dashboard de vendas, com foco na organização e visualização de dados.

O objetivo é transformar dados brutos em informações visuais claras e úteis, permitindo uma análise eficaz do desempenho de vendas e a tomada de decisões baseadas em dados.

---

**Dashboard de Vendas do Xbox Game Pass**

Este projeto tem como objetivo transformar dados brutos em informações visuais claras e úteis, permitindo uma análise eficaz do desempenho de vendas do Xbox Game Pass e auxiliando na tomada de decisões baseadas em dados.

O trabalho foi desenvolvido em Excel, utilizando tabelas dinâmicas, gráficos interativos, segmentações (Slicers) e boas práticas de design de dashboards.

---

<img width="869" height="1346" alt="Screenshot_20251127-113700" src="https://github.com/user-attachments/assets/2de5a577-79ea-4365-a3fe-bb00cb77d8b3" />


---


📑 **Explicação de cada pasta e arquivo**

**Pasta data/**
- **base01.xlsx** → Base de dados original com informações de assinantes, planos, preços, add-ons e valores totais.
- **baseDados.md** → Documento explicativo sobre a estrutura da base.
- **dicionario_dados.md** → Versão em Markdown do dicionário de dados.
- **dicionariodedados.xlsx** → Planilha com três abas:
  - **Dicionário de Dados:** descrição detalhada de cada coluna.
  - **Notas de Uso:** regras e observações sobre os dados.
  - **Glossário:** termos técnicos usados no projeto.

**Pasta dashboards/**
- **dashboardxboxfinalizado01.xlsx** → Dashboard finalizado com KPIs e gráficos interativos.
- **Dashboard_Vendas.xlsx** → Versão de trabalho do dashboard.
- **dash.md** → Documento explicativo sobre a construção dos dashboards.

**Pasta docs/**
- **metodologia_ABCDE.md** → Explicação detalhada da metodologia ABCDE aplicada ao projeto.
- **design_system.md** → Guia de design (cores, tipografia, layout).
- **checklist_qa.md** → Lista de verificação de qualidade para validar o dashboard.
- **capturas/** → Imagens ilustrativas do dashboard:
  - **dashboard_xbox.png** → Visão geral do dashboard.
  - **desempenho_vendas_xbox.png** → Gráfico de desempenho de vendas.
  - **dashboard_kpi_xbox.png** → KPIs principais (planos, receita, add-ons).
  - **evolucao_mensal_faturamento.png** → Evolução mensal do faturamento.
  - **mensal_planos_xboxgame_pass.png** → Gráfico de barras empilhadas mostrando participação dos planos.
  - **kpi_estrategico_faturamento.png** → Painel estratégico com KPIs e distribuições.
- **imagens.md** → Documento explicativo sobre as imagens.

**Pasta scripts/**
- **formulas_e_dicas.md** → Guia prático com fórmulas do Excel (SUMIFS, colunas auxiliares, normalização) e dicas de uso.

---

🧩 **Tecnologias utilizadas**

- Microsoft Excel 2016+ / Excel 365
  - Tabelas dinâmicas (Pivot Tables).
  - Segmentações (Slicers).
  - Gráficos dinâmicos (colunas, barras, pizza).
  - Fórmulas: SUMIFS, IF, TEXT.
- Git/GitHub
  - Versionamento de arquivos e documentação.
- Markdown
  - Documentação clara e estruturada (README.md, docs/*.md).

---

💻 **Requisitos de Hardware e Software**

**Hardware**
- CPU dual-core ou superior.
- 4 GB RAM (8 GB recomendado).
- ~200 MB de espaço livre para arquivos e imagens.

**Software**
- Microsoft Excel 2016 ou superior (recomendado Excel 365).
- Navegador atualizado para acessar o GitHub.
- Git instalado (opcional, para clonagem do repositório).

---

📐 **Método ABCDE aplicado**

**A — Avaliar**
- Objetivo: criar um dashboard que responda perguntas de negócio sobre vendas e assinaturas do Xbox Game Pass.
- Perguntas principais:
  - P1: Faturamento total de vendas de planos anuais.
  - P2: Faturamento anual separado por auto-renovação.
  - P3: Total de vendas de assinaturas do EA Play.
  - P4: Total de vendas de assinaturas do Minecraft Season Pass.

**B — Base**
- Arquivo de origem: data/base01.xlsx.
- Colunas essenciais: Subscriber ID, Name, Plan, Start Date, Auto Renewal, Subscription Price, Subscription Type, EA Play Season Pass, EA Play Season Pass Price, Minecraft Season Pass, Minecraft Season Pass Price, Coupon Value, Total Value.
- Observações: valores “-” tratados como 0; flags Yes/No; Total Value já calculado.

**C — Calcular**
- Métricas-chave:
  - Faturamento Anual (P1).
  - Faturamento Anual por Auto Renewal (P2).
  - Vendas EA Play (P3).
  - Vendas Minecraft (P4).
- Segmentações úteis: por plano, mês, auto-renovação, cupom.

**D — Design**
- Paleta de cores:
  - Xbox Color: #9BC848, #22C55E, #2AE6B1
  - Menus: #5BF6A8
  - Neutro: #E8E6E9
- Regras:
  - Big numbers em destaque.
  - Gráficos limpos, sem gridlines.
  - Filtros laterais consistentes.
  - Títulos explicativos e rótulos diretos.

**E — Entregar**
- Arquivos finais: dashboards/dashboardxboxfinalizado01.xlsx, README.md, imagens em docs/capturas.
- Publicação: repositório GitHub Santosdevbjj/vendasXboxExcelDash.

---

• **Conclusão**

Este projeto demonstra como aplicar boas práticas de Ciência de Dados e Data Visualization em Excel, documentando de forma profissional e clara.  
A estrutura organizada, o método ABCDE e os arquivos complementares garantem reprodutibilidade, clareza e valor de negócio.

---

**Autor:**
Sergio Santos 


---


**Contato:**


[![Portfólio Sérgio Santos](https://img.shields.io/badge/Portfólio-Sérgio_Santos-111827?style=for-the-badge&logo=githubpages&logoColor=00eaff)](https://santosdevbjj.github.io/portfolio/)
[![LinkedIn Sérgio Santos](https://img.shields.io/badge/LinkedIn-Sérgio_Santos-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/santossergioluiz) 



---

