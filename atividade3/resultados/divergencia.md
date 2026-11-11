# Divergências entre métrica automática e avaliação humana

Análise das divergências F1–R1 e R1–R2 após consolidar os dados observados; não interpretar métricas automáticas como julgamento humano.

## Tarefa

Identificar divergências entre o sinal exploratório de F1 lexical e as aprovações R1 reportadas, sem tratar a métrica automática como julgamento humano.

## F1 automático versus R1

Com `tau = 0,5`, o sinal automático aprovou 2/6 respostas A (CT02 e CT06) e 3/6 respostas B (CT02, CT05 e CT06). R1 reporta aprovação para as 12 respostas. Assim, houve concordância em 5/12: A-CT02, A-CT06, B-CT02, B-CT05 e B-CT06. Nas outras sete (A-CT01, A-CT03, A-CT04, A-CT05, B-CT01, B-CT03 e B-CT04), R1 aprovou e o limiar automático não.

## R1 versus R2

O estudante informou que R2 revisou CT01 e CT05 nas duas versões e atribuiu os mesmos escores de R1 nas quatro saídas: concordância de decisões **4/4**. Nenhuma divergência foi reportada; portanto, não houve consenso formal. A justificativa geral reportada foi “Respostas Esperadas e Condizentes”, sem evidência individual anexada. Esse resultado não se estende às outras oito saídas.

## Análise do artefato

Os dados de R1 são os escores reportados pelo estudante e transcritos em `r1.csv`; fichas e justificativas por resposta não foram anexadas, e a rubrica foi formalizada após a coleta. O estudante relata revisão humana das referências, mas nome e data não foram registrados e a revisão não foi verificada independentemente. `tau = 0,5` foi escolhido após as execuções. Portanto, a divergência é descritiva/exploratória e não valida nem invalida por si só a avaliação humana. F1 lexical mede sobreposição de tokens, não semântica, correção ou suporte factual.

## Resultados

As médias F1 foram 0,479003 (A) e 0,503373 (B); as medianas foram 0,454726 (A) e 0,494036 (B). A diferença descritiva entre médias é 0,024370 a favor de B, mas não permite concluir superioridade: o conjunto tem apenas seis casos, o limiar é pós-hoc e os prompts/configurações não estão comprovados por captura. R1 aprovou 6/6 em ambas as versões, sem diferença de aprovação humana reportada. R1–R2 teve concordância reportada de 4/4 somente nas duas perguntas selecionadas por versão.
