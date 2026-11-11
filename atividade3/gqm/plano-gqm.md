# Plano GQM

Registrar e congelar este plano antes da execução dos testes; preencher os campos em aberto antes de coletar resultados.

## Tarefa

Avaliar métricas automáticas versus avaliação humana e o ciclo de vida/versionamento do fluxo de Base de Conhecimento do Cherry Studio, comparando duas versões que diferem somente no prompt de sistema.

## Objetivo

- Analisar: as respostas do fluxo de Base de Conhecimento (RAG) do Cherry Studio.
- Com o propósito de: comparar a qualidade humana entre a versão A (baseline) e a versão B (mudança apenas no prompt de sistema) e verificar se o sinal automático acompanha a adequação julgada por pessoas.
- Com respeito a: correção, relevância, suporte nas fontes, aprovação humana e concordância entre F1 lexical e avaliação humana.
- Do ponto de vista de: equipe de avaliação da disciplina Qualidade de Software.
- No contexto de: seis casos CT01–CT06, cada um executado uma vez nas versões A e B, totalizando 12 saídas; R1 avalia as 12 e R2 revisa CT01 e CT05 nas duas versões.

## Q1 — Qualidade das respostas

**A versão B atende melhor do que a versão A em qualidade humana?** Comparar a quantidade de saídas aprovadas por R1 em cada versão, com denominador 6 por versão e a regra de aprovação abaixo. A conclusão é descritiva para os seis casos; não generalizar além do experimento.

## Q2 — Concordância entre avaliações

**O sinal automático baseado em F1 lexical representa a adequação das respostas conforme a avaliação humana?** Comparar o sinal binário automático ao resultado humano de R1 nas 12 saídas. A concordância R1–R2 nas quatro revisões é uma medida separada de consistência entre revisores, não substitui a comparação automático–humano.

## Medidas

As três medidas GQM são F1 lexical, taxa de aprovação humana e concordância automático–humano. A concordância R1–R2 é uma verificação suplementar de consistência dos revisores, com quatro casos, e não deve ser confundida com a terceira medida.

| Medida | Unidade | Fórmula/denominador | Limitação |
|---|---|---|---|
| F1 lexical automático | Escore de 0 a 1 por saída; sinal aprova se `F1 >= tau` | Tokens normalizados em NFC e `casefold`; precisão e revocação calculadas pela interseção de multiconjuntos; `F1 = 2 × precisão × revocação / (precisão + revocação)`. Calcular por saída; aprovação por versão usa 6 saídas. | Sobreposição lexical não garante correção semântica nem suporte factual; sensível à referência e à tokenização. |
| Aprovação humana (R1) | Proporção e percentual por versão | Número de saídas aprovadas por R1 / 6 saídas da versão. Aprovada somente com correção=2, relevância=2, suporte=2 e falha crítica=0. | Uma revisão principal por saída; julgamento depende da rubrica e da referência. |
| Concordância automático–humano | Proporção e percentual | Número de saídas em que o sinal automático (`F1 >= tau`) coincide com a decisão de aprovação de R1 / 12 saídas. | Concordância não prova validade da métrica; o conjunto é pequeno e a decisão humana depende da rubrica e das referências. |

Como análise suplementar, calcular concordância R1–R2 como decisões iguais / 4 saídas (CT01 e CT05 nas versões A e B), antes de qualquer consenso. Registrar eventual consenso separadamente e sem substituir as notas originais.

### Limiar automático (`tau`)

O relatório fornecido informa que Raphael fixou `tau` antes das execuções, mas não informa o valor escolhido. **Transcrever o valor exato do plano pré-teste original:** `[PREENCHER: confirmar com Raphael; a informação disponível não permite afirmar se foi 0,5 ou outro valor justificado]`. Não escolher nem alterar o limiar após consultar os resultados.

## Regra de falha crítica

Registrar falha crítica como 0 (ausente) ou 1 (presente). Qualquer falha crítica (1) reprova a saída, independentemente das notas; para aprovação, as três notas devem ser 2 e a falha crítica deve ser 0.

## Critério de avanço

O relatório fornecido confirma que Raphael definiu um critério de avanço antes das execuções, mas não informa seu conteúdo. **Transcrever o critério aprovado no plano pré-teste original:** [PREENCHER: confirmar com Raphael]. Não criar um critério retroativo nem tratar a decisão experimental como autorização para produção.

## Condição de bloqueio

O relatório fornecido confirma que Raphael definiu uma condição de bloqueio antes das execuções, mas não informa seu conteúdo. **Transcrever a condição aprovada no plano pré-teste original:** [PREENCHER: confirmar com Raphael]. A regra de falha crítica já registrada neste documento permanece: qualquer saída com falha crítica reprova individualmente; confirmar no plano original se também constituía bloqueio da versão.

## Registro pré-teste

- Data de registro do plano: [PREENCHER: consultar o commit/registro original; não consta no trecho fornecido].
- Responsável pelo registro: Raphael Portella (conforme a divisão de tarefas informada).
- Evidência de que o plano foi registrado antes da execução: o relatório afirma que as regras foram fixadas antes das execuções; vincular o commit original e conferir sua data em relação à primeira execução: [PREENCHER].

## Análise do artefato

O relatório informa que o plano, o limiar, a rubrica, as regras e os casos foram preparados por Raphael antes das execuções. No clone atual, porém, não há o commit pré-teste nem os valores completos: `tau`, critério de avanço, condição de bloqueio e referências dos casos ainda precisam ser transcritos do artefato original e confrontados com a data da primeira execução. Até essa verificação, este arquivo atualizado não deve ser apresentado como prova de pré-registro.

## Resultados

[PREENCHER após executar os casos; não inserir resultados antes da coleta.]
