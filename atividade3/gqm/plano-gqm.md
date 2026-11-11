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

O estudante solicitou definir `tau` depois de executar e ver as respostas. Para uma análise **exploratória pós-hoc**, adota-se `tau = 0,5`, opção mencionada no enunciado. Isso não comprova nem substitui um limiar pré-registrado e não deve ser apresentado como critério fixado antes das execuções. O valor original informado como pré-teste por Raphael continua não confirmado.

## Regra de falha crítica

Registrar falha crítica como 0 (ausente) ou 1 (presente). Qualquer falha crítica (1) reprova a saída, independentemente das notas; para aprovação, as três notas devem ser 2 e a falha crítica deve ser 0.

## Critério de avanço

O conteúdo do critério atribuído a Raphael não foi fornecido. Não há critério de avanço verificável neste repositório. Não criar um critério retroativo com base nos resultados nem tratar a decisão experimental como autorização para produção.

## Condição de bloqueio

O conteúdo da condição atribuída a Raphael não foi fornecido. Não há condição de bloqueio pré-registrada verificável neste repositório. A regra de falha crítica descrita neste esqueleto não permite inferir, retroativamente, o bloqueio originalmente definido para a versão.

## Registro pré-teste

- Data de registro do plano: 10/11/2026, conforme informação do estudante; arquivo/commit original que comprove o registro antes dos testes: [NÃO FORNECIDO].
- Responsável pelo registro: Raphael Portella (conforme a divisão de tarefas informada).
- Evidência de que o plano foi registrado antes da execução: relatório e estudante declaram que o plano estava registrado em 10/11/2026; não foi apresentada evidência versionada original. As execuções relatadas ocorreram em 11/11/2026.

## Análise do artefato

O relatório e o estudante atribuem a Raphael um plano preparado em 10/11/2026, antes das respostas de 11/11/2026. Contudo, o arquivo/commit original não foi fornecido, e os valores do limiar original e dos critérios não foram informados. O `tau = 0,5` registrado acima é pós-hoc e exploratório; este arquivo atualizado não é prova de pré-registro. As referências em uso também foram geradas como rascunhos com auxílio de IA e não atendem à exigência de referências escritas por uma pessoa.

## Resultados

[PREENCHER após executar os casos; não inserir resultados antes da coleta.]
