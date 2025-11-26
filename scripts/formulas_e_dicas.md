# Fórmulas e Dicas para o Dashboard de Vendas do Xbox

Este documento reúne as principais fórmulas utilizadas no projeto e dicas práticas para trabalhar com dados no Excel.  
O objetivo é facilitar a reprodução e manutenção do dashboard.

---

## 1. Fórmulas essenciais

### 1.1. Normalização de valores
Em algumas colunas (como preços de Season Pass), o valor “-” deve ser tratado como 0.

```excel
=IF(A2="-";0;A2)


---


- Uso: substituir valores inválidos por zero.
- Aplicação: colunas EA Play Season Pass Price e Minecraft Season Pass Price.

```
---

**1.2. Derivar o mês da assinatura**
Para criar análises mensais, derive o mês a partir da data de início.

`excel
=TEXT([@Start Date];"YYYY-MM")
`

- Uso: gera uma coluna auxiliar “Month”.
- Aplicação: facilita filtros e segmentações por período.

---

**1.3. Identificar se há cupom**
Crie uma flag para indicar se o assinante utilizou cupom.

`excel
=IF([@Coupon Value]>0;"Yes";"No")
`

- Uso: coluna auxiliar “Has Coupon”.
- Aplicação: segmentação de vendas com/sem desconto.

---

**1.4. Faturamento total de planos anuais**
`excel
=SUMIFS(tblSubscriptions[Total Value];tblSubscriptions[Subscription Type];"Annual")
`

- Uso: soma o valor total apenas para assinaturas anuais.
- Aplicação: KPI principal do dashboard.

---

**1.5. Faturamento anual por auto-renovação**
`excel
=SUMIFS(tblSubscriptions[Total Value];tblSubscriptions[Subscription Type];"Annual";tblSubscriptions[Auto Renewal];"Yes")
`

`excel
=SUMIFS(tblSubscriptions[Total Value];tblSubscriptions[Subscription Type];"Annual";tblSubscriptions[Auto Renewal];"No")
`

- Uso: separa faturamento anual entre assinaturas com e sem auto-renovação.
- Aplicação: análise de retenção e fidelização.

---

**1.6. Total de vendas do EA Play**
`excel
=SUMIFS(tblSubscriptions[EA Play Season Pass Price];tblSubscriptions[EA Play Season Pass];"Yes")
`

- Uso: soma apenas os preços de Season Pass quando ativo.
- Aplicação: KPI de vendas adicionais.

---

**1.7. Total de vendas do Minecraft Season Pass**
`excel
=SUMIFS(tblSubscriptions[Minecraft Season Pass Price];tblSubscriptions[Minecraft Season Pass];"Yes")
`

- Uso: soma apenas os preços de Season Pass do Minecraft.
- Aplicação: KPI de vendas adicionais.

---

**2. Dicas práticas de Excel**

**2.1. Tabelas estruturadas**
- Transforme a base em Tabela (Ctrl + T).
- Nomeie como tblSubscriptions.
- Vantagens:
  - Fórmulas dinâmicas (não precisam de intervalos fixos).
  - Facilidade para criar Pivots.
  - Atualização automática ao adicionar linhas.

---

**2.2. Tabelas dinâmicas (Pivots)**
- Use Pivots para responder perguntas de negócio.
- Configure filtros (Subscription Type, Auto Renewal).
- Use Slicers para interatividade.
- Sempre configure valores como Soma, não Contagem.

---

**2.3. Big Numbers**
- Crie células com fórmulas de KPIs (ex.: Total Anual).
- Vincule caixas de texto no dashboard a essas células.
- Formate em verde principal (#9BC848) e tamanho grande.

---

**2.4. Segmentações (Slicers)**
- Adicione Slicers para:
  - Plan (Core, Standard, Ultimate).
  - Auto Renewal (Yes/No).
  - Subscription Type (Monthly, Quarterly, Annual).
  - Month (coluna auxiliar).
- Estilize com cores da paleta (Menus: #5BF6A8).

---

**2.5. Formatação condicional**
- Use para destacar valores acima da média.
- Exemplo: colunas de Total Value com gradiente verde.
- Ajuda a identificar assinaturas de maior valor.

---

**2.6. Organização visual**
- Remova linhas de grade na aba Dashboard.
- Use caixas de texto para títulos e notas de contexto.
- Mantenha alinhamento e espaçamento consistentes.

---

**3. Boas práticas**

- Consistência: use sempre a mesma paleta e tipografia.
- Documentação: mantenha fórmulas explicadas neste arquivo.
- Validação: compare resultados de fórmulas com Pivots.
- Performance: evite fórmulas voláteis; prefira SUMIFS e tabelas dinâmicas.
- Backup: salve versões em dashboards/ com nomes incrementais (v1, v2, final).

---

**4. Conclusão**

Este guia de fórmulas e dicas garante que:
- Os cálculos sejam reproduzíveis e confiáveis.
- O dashboard seja interativo e visualmente claro.
- A manutenção futura seja simples e bem documentada.

Use este arquivo como referência rápida sempre que precisar revisar ou atualizar o projeto.
`

---

 







