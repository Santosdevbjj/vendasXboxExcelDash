
 **Dicionário de Dados**

| Campo                     | Descrição                                                                 | Tipo de Dado | Exemplo            | Observações                                                                 |
|--------------------------------|-------------------------------------------------------------------------------|------------------|------------------------|---------------------------------------------------------------------------------|
| Subscriber ID                  | Identificador único do assinante                                              | Numérico (Inteiro) | 3231                   | Não se repete; chave primária da base.                                          |
| Name                           | Nome completo do assinante                                                    | Texto             | João Silva             | Usado apenas para referência; não é utilizado em cálculos.                      |
| Plan                           | Tipo de plano contratado                                                      | Texto (Categoria) | Ultimate, Standard, Core | Três categorias possíveis.                                                      |
| Start Date                     | Data de início da assinatura                                                  | Data              | 01/01/2024             | Usada para análises temporais (mensal, trimestral, anual).                      |
| Auto Renewal                   | Indica se a assinatura tem renovação automática                               | Texto (Yes/No)    | Yes                    | Permite análise de retenção e fidelização.                                      |
| Subscription Price             | Valor base da assinatura                                                      | Numérico (Moeda)  | 15                     | Valor mensal, trimestral ou anual, dependendo do tipo.                          |
| Subscription Type              | Periodicidade da assinatura                                                   | Texto             | Monthly, Quarterly, Annual | Define o ciclo de cobrança.                                                     |
| EA Play Season Pass            | Indica se o assinante possui o add-on EA Play                                 | Texto (Yes/No)    | Yes                    | Flag binária.                                                                   |
| EA Play Season Pass Price      | Valor do add-on EA Play                                                       | Numérico (Moeda)  | 30                     | Se não contratado, deve ser 0.                                                  |
| Minecraft Season Pass          | Indica se o assinante possui o add-on Minecraft                               | Texto (Yes/No)    | No                     | Flag binária.                                                                   |
| Minecraft Season Pass Price    | Valor do add-on Minecraft                                                     | Numérico (Moeda)  | 20                     | Se não contratado, deve ser 0.                                                  |
| Coupon Value                   | Valor de desconto aplicado                                                    | Numérico (Moeda)  | 5                      | Se não houver cupom, valor = 0.                                                 |
| Total Value                    | Valor total da assinatura (base + add-ons – cupom)                            | Numérico (Moeda)  | 60                     | KPI principal para faturamento.                                                 |
| Month (coluna derivada)        | Mês/ano da assinatura                                                         | Texto (YYYY-MM)   | 2024-01                | Criada via fórmula =TEXT([@Start Date];"YYYY-MM").                            |
| Has Coupon (coluna derivada)   | Indica se houve cupom aplicado                                                | Texto (Yes/No)    | Yes                    | Criada via fórmula =IF([@Coupon Value]>0;"Yes";"No").                         |

---

Aba: Notas de Uso

| Nota                                                                 | Explicação                                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Valores “-” devem ser tratados como 0                                     | Evita erros em cálculos de add-ons.                                             |
| Total Value já está calculado na base                                   | Inclui assinatura + add-ons – cupom.                                            |
| Month e Has Coupon são colunas auxiliares                            | Não existem na base original, mas devem ser criadas para análises.              |
| Auto Renewal é crítico para segmentação                                | Permite separar assinaturas que se renovam automaticamente das que não renovam. |
| Plan deve ser usado como categoria principal                           | Core, Standard e Ultimate são os três níveis de assinatura.                     |
| Sempre validar tipos de dados antes de criar Pivots                      | Datas como Data, valores como Número, flags como Texto.                         |

---

Aba: Glossário

| Termo             | Definição                                                                 |
|------------------------|-------------------------------------------------------------------------------|
| KPI                   | Key Performance Indicator (Indicador-chave de desempenho).                    |
| Big Number            | Valor numérico destacado no dashboard, representando uma métrica principal.   |
| Pivot Table           | Tabela Dinâmica do Excel usada para sumarizar e analisar dados.               |
| Slicer                | Filtro visual do Excel que permite segmentar dados dinamicamente.             |
| Data View             | Camada organizada da base de dados, pronta para análise.                      |

---
