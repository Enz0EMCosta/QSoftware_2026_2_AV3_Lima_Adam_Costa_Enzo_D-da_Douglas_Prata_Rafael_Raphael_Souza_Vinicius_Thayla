# Decisão experimental

Registrar a conclusão descritiva sobre A e B e distinguir resultados observados de critérios e limitações conhecidos após a coleta.

## Tarefa

Responder se os dados descritivos disponíveis apoiam manter A, considerar B para uma nova avaliação ou declarar o experimento inconclusivo.

## Evidências consideradas

- Plano GQM: `atividade3/gqm/plano-gqm.md`; o plano original/commit pré-teste não foi fornecido.
- Tabela consolidada: `atividade3/resultados/tabela-consolidada.csv`.
- Análise de divergência: `atividade3/resultados/divergencia.md`.
- Gráfico: `atividade3/resultados/grafico-resultados.svg`.
- R2: quatro notas transcritas do relato do estudante; concordância R1–R2 reportada 4/4.
- Manifestos: `atividade3/versoes/A/manifesto.md` e `atividade3/versoes/B/manifesto.md`.

## Resultados

Há 12 respostas textuais registradas, seis por versão. O estudante reporta escores de R1 iguais a correção=2, relevância=2, suporte=2 e falha crítica=0 em todas as respostas; isso corresponde provisoriamente a aprovação R1 de 6/6 em A e 6/6 em B. As justificativas individuais não foram fornecidas e os descritores foram formalizados depois da coleta.

O cálculo lexical exploratório, contra `casos-e-referencias2.csv` e com `tau=0,5` escolhido pós-hoc, resultou em F1 médio 0,479003 para A e 0,503373 para B; o sinal automático aprovou 2/6 respostas A e 3/6 B. A concordância entre sinal automático e R1 reportado foi 5/12. R1 aprovou 6/6 em cada versão. R1–R2 concordaram em 4/4 decisões reportadas nas revisões CT01 e CT05 em A e B. As justificativas de R2 foram gerais, sem evidência individual anexada. O relato de revisão humana das referências não inclui nome/data nem comprovação independente. Esses números não demonstram superioridade de B nem substituem avaliação humana.

## Decisão

**Decisão experimental: inconclusiva; não recomendar adoção de B nem declarar superioridade confirmada.** R1 reporta 6/6 aprovações em A e 6/6 em B segundo escores 2,2,2,0 transcritos; isso não mostra diferença de aprovação humana entre as versões. R1–R2 concordaram em 4/4 decisões reportadas, mas com justificativa geral e sem fichas anexadas. O F1 médio foi numericamente 0,024370 maior em B, porém `tau=0,5` foi escolhido pós-hoc, há somente seis casos por versão e F1 mede sobreposição lexical. A concordância exploratória automático–R1 foi 5/12. Os prompts distintos foram informados após as execuções e não há capturas/configurações arquivadas para verificar a aplicação consistente da mudança. Isso não é autorização de produção.

**Critério de continuação definido após a coleta:** considerar B somente para uma nova avaliação confirmatória se sua aprovação humana não for inferior à de A e se não houver falha crítica reportada em B. Pelos resultados reportados, B satisfaz esses requisitos exploratórios (6/6 contra 6/6; nenhuma falha crítica reportada). Como o critério foi definido após observar os resultados, ele não substitui pré-registro e não autoriza adoção ou produção; apenas orienta uma possível nova etapa.

## Limitações e validade

Uma execução por caso/versão; alias `latest` não congelável; quatro capturas parciais não mostram os prompts nem a configuração completa; prompts diferentes foram relatados após as execuções, sem confirmação independente de que só o prompt mudou; parâmetros, igualdade de base e a maioria dos contextos recuperados não demonstrados. Fontes sintéticas preparadas com IA; a captura B-CT04 mostra aviso de revisão/aprovação pendente e campos editoriais “PREENCHER” em DOC-04, sem prova de aprovação antes do teste. A revisão humana posterior das referências é autorrelato sem nome/data. Fichas originais ausentes, justificativas R1 específicas ausentes e R2 com justificativa geral; rubrica operacional formalizada depois da coleta; `tau` e critério operacional pós-hoc; critério original não fornecido.

## Acompanhamento

Para nova avaliação confirmatória, revisar as referências, a rubrica, os prompts e o protocolo com pessoas, pré-registrar os critérios e preservar capturas/contextos; identificar qualquer execução adicional como nova coleta, sem misturá-la retroativamente com as respostas já registradas. A presente evidência não basta para adoção ou produção.

## Análise do artefato

Os valores foram reconciliados com a tabela consolidada e os arquivos R1/R2. Quatro capturas foram recebidas e arquivadas: duas mostram A-CT01/A-CT02, uma B-CT02 e uma B-CT04 com painel da fonte. São evidências parciais, não comprovam prompts/configuração ou o contexto de todas as saídas. As avaliações humanas permanecem autorrelatos transcritos, sem fichas originais anexadas.
