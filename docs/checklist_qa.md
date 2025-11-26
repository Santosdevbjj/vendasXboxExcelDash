**Checklist de qualidade do dashboard**

Este checklist garante que o dashboard de vendas do Xbox esteja correto, consistente e pronto para uso e apresentação. Use-o antes de publicar ou compartilhar o arquivo para evitar surpresas.

---

**Preparação dos dados**

- Tipos de dados: verifique que datas, números e textos estão corretamente tipados nas colunas.
- Valores faltantes: substitua “-” por 0 nas colunas de preço de add-ons.
- Integridade: confirme que Subscriber ID é único e não há duplicidades inesperadas.
- Colunas auxiliares: valide “Month” e “Has Coupon” com amostragem manual.
- Tabela estruturada: confirme que a área de dados é uma tabela (tblSubscriptions) com cabeçalhos corretos.

---

**Métricas e cálculos**

- Total anual: teste a soma de Total Value com Subscription Type = Annual (SUMIFS e Pivot concordam).
- Auto-renovação: compare valores Yes vs No para Annual; verifique totais e percentuais.
- EA Play: confira soma de EA Play Season Pass Price quando flag = Yes; valores “-” convertidos em 0.
- Minecraft: confirme soma de Minecraft Season Pass Price quando flag = Yes; mesma regra de 0.
- Cupons: valide que Coupon Value está subtraindo corretamente (quando aplicável) no Total Value.
- Amostragem: selecione 5–10 linhas aleatórias e re-calcule manualmente o Total Value.

---

**Tabelas dinâmicas**

- Filtros corretos: cada Pivot usa filtros condizentes com a pergunta (ex.: Annual para P1/P2).
- Campos de valores: Soma (não contagem) para métricas monetárias.
- Atualização: “Atualizar Tudo” reflete corretamente mudanças na Data_View.
- Consistência: Pivots têm formatos numéricos uniformes (moeda, separadores de mil).
- Nomes: nomeie Pivots conforme sua função (ex.: PivotAnnualRevenue, Pivot_EAPlay).

---

**Gráficos e visualizações**

- Big numbers: cartões exibem valores corretos e vinculados a células confiáveis (Calc ou Pivot).
- Rótulos: rótulos de dados estão ativados e legíveis; sem sobreposição.
- Eixos: limites e escalas adequados; sem distorção visual.
- Cores: paleta aplicada corretamente (ver design system); contraste suficiente.
- Legendas: presentes somente quando necessárias; evite redundância.
- Interação: gráficos reagem aos Slicers; não ficam “vazios” sem mensagem clara.

---

**Filtros e interatividade**

- Slicers vinculados: todos os Slicers estão conectados às Pivots relevantes.
- Estado inicial: filtros começam em “Todos” ou em um estado de análise definido e útil.
- Organização: Slicers alinhados horizontalmente; tamanhos e estilos consistentes.
- Desempenho: aplicar múltiplos filtros não causa lentidão excessiva.

---

**Layout e design**

- Estrutura: título no topo, filtros abaixo, big numbers, gráficos por pergunta.
- Grade visual: alinhamentos, espaçamentos e margens consistentes; sem linhas de grade.
- Tipografia: tamanhos e pesos conforme design system; títulos claros e objetivos.
- Cores: aplicação fiel à paleta; uso de neutros para fundos e destaques para KPIs.
- Info context: cada número relevante tem uma nota de escopo (ex.: “Somente Annual”).

---

**Usabilidade e narrativa**

- Perguntas respondidas: P1–P4 são facilmente encontradas e respondidas visualmente.
- Tempo de entendimento: um usuário deve entender os KPIs principais em menos de 10 segundos.
- Mensagens de erro: se um filtro zerar um gráfico, mostrar texto informativo (“Sem dados para o filtro selecionado”).
- Rótulos: sem jargão; linguagem direta e consistente.

---

**Validação cruzada**

- Coerência: resultados das Pivots batem com cálculos em Calc (diferença zero).
- Exportação: capturas de tela em docs/capturas estão atualizadas com a versão atual.
- Versão: nome do arquivo reflete o estado (ex.: dashboardxboxv1.xlsx).

---

**Performance e manutenção**

- Tamanho do arquivo: manter dentro de um limite aceitável; remover abas não utilizadas.
- Atualização de dados: processo claro para atualizar Data_View sem quebrar Pivots.
- Dependências: evitar fórmulas voláteis; documentar quaisquer macros (se existirem).
- Backups: manter cópias versões anteriores em dashboards/.

---

**Publicação e documentação**

- README: atualizado com instruções, estrutura e como reproduzir.
- Design system: alinhado com o que foi implementado no dashboard.
- Metodologia: metodologia_ABCDE.md descreve fielmente o processo seguido.
- Arquivos de apoio: base01.xlsx e dashboardxboxfinalizado01.xlsx presentes em seus caminhos.
- Licença: arquivo LICENSE incluído, se aplicável.

---

**Teste rápido final (5 minutos)**

- Abertura: abrir o arquivo sem alertas ou links quebrados.
- Atualizar tudo: executar e verificar que os números permanecem consistentes.
- Aplicar filtros: selecionar um mês e um plano; checar se todos os gráficos reagem.
- Conferir KPIs: ler os quatro KPIs principais; validar valores esperados.
- Salvar: garantir que o arquivo mantém formatação e links ao fechar e abrir novamente.

---

**Aprovação**

- Critérios de aprovação: todas as seções acima marcadas como OK.
- Registro: documentar data, versão e responsável pela revisão no docs/checklist_qa.md.
- Observações finais: anotar qualquer melhoria futura (ex.: adicionar Power Query, novos KPIs, segmentação por região).

> **Dica:** use este checklist como parte do fluxo padrão de versionamento. Ele evita retrabalho e dá confiança para quem vai consumir o dashboard.

   
