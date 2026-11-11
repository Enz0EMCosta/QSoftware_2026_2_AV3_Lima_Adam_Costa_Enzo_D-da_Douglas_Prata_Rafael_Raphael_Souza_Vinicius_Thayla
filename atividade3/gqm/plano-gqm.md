# Plano GQM

Registrar e congelar este plano antes da execução dos testes; preencher os campos em aberto antes de coletar resultados.

## Tarefa

Avaliar métricas automáticas versus avaliação humana e o ciclo de vida/versionamento do fluxo de Base de Conhecimento do Cherry Studio, comparando duas versões que diferem somente no prompt de sistema.

## Objetivo

- Analisar: [PREENCHER: objeto e atributo de qualidade].
- Com o propósito de: [PREENCHER].
- Com respeito a: qualidade das respostas, suporte nas fontes e concordância entre sinais.
- Do ponto de vista de: [PREENCHER: perspectiva].
- No contexto de: seis casos CT01–CT06, cada um executado nas versões A e B.

## Q1 — Qualidade das respostas

[PREENCHER: pergunta de pesquisa sobre as aprovações automáticas e humanas nas versões A e B.]

## Q2 — Concordância entre avaliações

[PREENCHER: pergunta de pesquisa sobre concordância F1–R1 e R1–R2.]

## Medidas

As três medidas abaixo cobrem F1 lexical, aprovação humana e concordância. A terceira reúne as duas comparações de concordância, que têm denominadores distintos.

| Medida | Unidade | Fórmula/denominador | Limitação |
|---|---|---|---|
| F1 lexical automático | Escore de 0 a 1 por saída; sinal aprova se `F1 >= tau` | Tokens normalizados em NFC e `casefold`; precisão e revocação calculadas pela interseção de multiconjuntos; `F1 = 2 × precisão × revocação / (precisão + revocação)`. Calcular por saída; aprovação por versão usa 6 saídas. | Sobreposição lexical não garante correção semântica nem suporte factual; sensível à referência e à tokenização. |
| Aprovação humana (R1) | Proporção e percentual por versão | Número de saídas aprovadas por R1 / 6 saídas da versão. Aprovada somente com correção=2, relevância=2, suporte=2 e falha crítica=0. | Uma revisão principal por saída; julgamento depende da rubrica e da referência. |
| Concordância | Proporção e percentual | F1 automático versus R1: decisões concordantes / 12 saídas. R1 versus R2: decisões concordantes / 4 saídas (CT01 e CT05 nas duas versões). Contabilizar eventual consenso separadamente, sem substituir avaliações originais. | R2 cobre apenas uma amostra de quatro saídas; a concordância binária não expressa a intensidade da divergência nem prova validade. |

### Limiar automático (`tau`)

`tau = [PREENCHER antes dos testes]`

## Regra de falha crítica

Registrar falha crítica como 0 (ausente) ou 1 (presente). Qualquer falha crítica (1) reprova a saída, independentemente das notas; para aprovação, as três notas devem ser 2 e a falha crítica deve ser 0.

## Critério de avanço

[PREENCHER antes dos testes: condição mensurável para avançar a versão B ou recomendar sua adoção.]

## Condição de bloqueio

[PREENCHER antes dos testes: condição que bloqueia a decisão ou a adoção, incluindo tratamento de falha crítica.]

## Registro pré-teste

- Data de registro do plano: [PREENCHER].
- Responsável pelo registro: [PREENCHER].
- Evidência de que o plano foi registrado antes da execução: [PREENCHER].

## Análise do artefato

[PREENCHER após verificar se o plano foi definido antes do teste, aplicado sem alterações retroativas e suficiente para reproduzir o cálculo.]

## Resultados

[PREENCHER após executar os casos; não inserir resultados antes da coleta.]
